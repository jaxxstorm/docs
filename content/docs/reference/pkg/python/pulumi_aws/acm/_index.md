---
title: Module acm
title_tag: Module acm | Package pulumi_aws | Python SDK
linktitle: acm
notitle: true
---

<div class="section" id="acm">
<h1>acm<a class="headerlink" href="#acm" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-aws/issues">pulumi/pulumi-aws repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws/issues">terraform-providers/terraform-provider-aws repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_aws.acm"></span><dl class="py class">
<dt id="pulumi_aws.acm.AwaitableGetCertificateResult">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.acm.</code><code class="sig-name descname">AwaitableGetCertificateResult</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">key_types</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">most_recent</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">statuses</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">types</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.AwaitableGetCertificateResult" title="Permalink to this definition">¶</a></dt>
<dd></dd></dl>

<dl class="py class">
<dt id="pulumi_aws.acm.Certificate">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.acm.</code><code class="sig-name descname">Certificate</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_authority_arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_body</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_chain</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">options</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">private_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">subject_alternative_names</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">validation_method</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.Certificate" title="Permalink to this definition">¶</a></dt>
<dd><p>The ACM certificate resource allows requesting and management of certificates
from the Amazon Certificate Manager.</p>
<p>It deals with requesting certificates and managing their attributes and life-cycle.
This resource does not deal with validation of a certificate but can provide inputs
for other resources implementing the validation. It does not wait for a certificate to be issued.
Use a <code class="docutils literal notranslate"><span class="pre">acm.CertificateValidation</span></code> resource for this.</p>
<p>Most commonly, this resource is used together with <code class="docutils literal notranslate"><span class="pre">route53.Record</span></code> and
<code class="docutils literal notranslate"><span class="pre">acm.CertificateValidation</span></code> to request a DNS validated certificate,
deploy the required validation records and wait for validation to complete.</p>
<p>Domain validation through E-Mail is also supported but should be avoided as it requires a manual step outside
of this provider.</p>
<p>It’s recommended to specify <code class="docutils literal notranslate"><span class="pre">create_before_destroy</span> <span class="pre">=</span> <span class="pre">true</span></code> in a <a class="reference external" href="https://www.terraform.io/docs/configuration/resources.html#lifecycle">lifecycle</a> block to replace a certificate
which is currently in use (eg, by <code class="docutils literal notranslate"><span class="pre">lb.Listener</span></code>).</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">cert</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">Certificate</span><span class="p">(</span><span class="s2">&quot;cert&quot;</span><span class="p">,</span>
    <span class="n">domain_name</span><span class="o">=</span><span class="s2">&quot;example.com&quot;</span><span class="p">,</span>
    <span class="n">tags</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;Environment&quot;</span><span class="p">:</span> <span class="s2">&quot;test&quot;</span><span class="p">,</span>
    <span class="p">},</span>
    <span class="n">validation_method</span><span class="o">=</span><span class="s2">&quot;DNS&quot;</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>
<span class="kn">import</span> <span class="nn">pulumi_tls</span> <span class="k">as</span> <span class="nn">tls</span>

<span class="n">example_private_key</span> <span class="o">=</span> <span class="n">tls</span><span class="o">.</span><span class="n">PrivateKey</span><span class="p">(</span><span class="s2">&quot;examplePrivateKey&quot;</span><span class="p">,</span> <span class="n">algorithm</span><span class="o">=</span><span class="s2">&quot;RSA&quot;</span><span class="p">)</span>
<span class="n">example_self_signed_cert</span> <span class="o">=</span> <span class="n">tls</span><span class="o">.</span><span class="n">SelfSignedCert</span><span class="p">(</span><span class="s2">&quot;exampleSelfSignedCert&quot;</span><span class="p">,</span>
    <span class="n">allowed_uses</span><span class="o">=</span><span class="p">[</span>
        <span class="s2">&quot;key_encipherment&quot;</span><span class="p">,</span>
        <span class="s2">&quot;digital_signature&quot;</span><span class="p">,</span>
        <span class="s2">&quot;server_auth&quot;</span><span class="p">,</span>
    <span class="p">],</span>
    <span class="n">key_algorithm</span><span class="o">=</span><span class="s2">&quot;RSA&quot;</span><span class="p">,</span>
    <span class="n">private_key_pem</span><span class="o">=</span><span class="n">example_private_key</span><span class="o">.</span><span class="n">private_key_pem</span><span class="p">,</span>
    <span class="n">subjects</span><span class="o">=</span><span class="p">[{</span>
        <span class="s2">&quot;commonName&quot;</span><span class="p">:</span> <span class="s2">&quot;example.com&quot;</span><span class="p">,</span>
        <span class="s2">&quot;organization&quot;</span><span class="p">:</span> <span class="s2">&quot;ACME Examples, Inc&quot;</span><span class="p">,</span>
    <span class="p">}],</span>
    <span class="n">validity_period_hours</span><span class="o">=</span><span class="mi">12</span><span class="p">)</span>
<span class="n">cert</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">Certificate</span><span class="p">(</span><span class="s2">&quot;cert&quot;</span><span class="p">,</span>
    <span class="n">certificate_body</span><span class="o">=</span><span class="n">example_self_signed_cert</span><span class="o">.</span><span class="n">cert_pem</span><span class="p">,</span>
    <span class="n">private_key</span><span class="o">=</span><span class="n">example_private_key</span><span class="o">.</span><span class="n">private_key_pem</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>certificate_authority_arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ARN of an ACMPCA</p></li>
<li><p><strong>certificate_body</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The certificate’s PEM-formatted public key</p></li>
<li><p><strong>certificate_chain</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The certificate’s PEM-formatted chain</p></li>
</ul>
</dd>
</dl>
<div class="highlight-default notranslate"><div class="highlight"><pre><span></span><span class="o">*</span> <span class="n">Creating</span> <span class="n">a</span> <span class="n">private</span> <span class="n">CA</span> <span class="n">issued</span> <span class="n">certificate</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>domain_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – A domain name for which the certificate should be issued</p></li>
<li><p><strong>options</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – Configuration block used to set certificate options. Detailed below.</p></li>
</ul>
</dd>
</dl>
<div class="highlight-default notranslate"><div class="highlight"><pre><span></span><span class="o">*</span> <span class="n">Importing</span> <span class="n">an</span> <span class="n">existing</span> <span class="n">certificate</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>private_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The certificate’s PEM-formatted private key</p></li>
<li><p><strong>subject_alternative_names</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of domains that should be SANs in the issued certificate. To remove all elements of a previously configured list, set this value equal to an empty list (<code class="docutils literal notranslate"><span class="pre">[]</span></code>).</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A map of tags to assign to the resource.</p></li>
<li><p><strong>validation_method</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Which method to use for validation. <code class="docutils literal notranslate"><span class="pre">DNS</span></code> or <code class="docutils literal notranslate"><span class="pre">EMAIL</span></code> are valid, <code class="docutils literal notranslate"><span class="pre">NONE</span></code> can be used for certificates that were imported into ACM and then into state managed by this provider.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>options</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">certificateTransparencyLoggingPreference</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies whether certificate details should be added to a certificate transparency log. Valid values are <code class="docutils literal notranslate"><span class="pre">ENABLED</span></code> or <code class="docutils literal notranslate"><span class="pre">DISABLED</span></code>. See <a class="reference external" href="https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html#concept-transparency">https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html#concept-transparency</a> for more details.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.arn">
<code class="sig-name descname">arn</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The ARN of the certificate</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.certificate_authority_arn">
<code class="sig-name descname">certificate_authority_arn</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.certificate_authority_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>ARN of an ACMPCA</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.certificate_body">
<code class="sig-name descname">certificate_body</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.certificate_body" title="Permalink to this definition">¶</a></dt>
<dd><p>The certificate’s PEM-formatted public key</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.certificate_chain">
<code class="sig-name descname">certificate_chain</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.certificate_chain" title="Permalink to this definition">¶</a></dt>
<dd><p>The certificate’s PEM-formatted chain</p>
<ul class="simple">
<li><p>Creating a private CA issued certificate</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.domain_name">
<code class="sig-name descname">domain_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.domain_name" title="Permalink to this definition">¶</a></dt>
<dd><p>A domain name for which the certificate should be issued</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.domain_validation_options">
<code class="sig-name descname">domain_validation_options</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.domain_validation_options" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of attributes to feed into other resources to complete certificate validation. Can have more than one element, e.g. if SANs are defined. Only set if <code class="docutils literal notranslate"><span class="pre">DNS</span></code>-validation was used.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">domain_name</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - A domain name for which the certificate should be issued</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceRecordName</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The name of the DNS record to create to validate the certificate</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceRecordType</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The type of DNS record to create</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceRecordValue</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The value the DNS record needs to have</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.options">
<code class="sig-name descname">options</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.options" title="Permalink to this definition">¶</a></dt>
<dd><p>Configuration block used to set certificate options. Detailed below.</p>
<ul class="simple">
<li><p>Importing an existing certificate</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">certificateTransparencyLoggingPreference</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies whether certificate details should be added to a certificate transparency log. Valid values are <code class="docutils literal notranslate"><span class="pre">ENABLED</span></code> or <code class="docutils literal notranslate"><span class="pre">DISABLED</span></code>. See <a class="reference external" href="https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html#concept-transparency">https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html#concept-transparency</a> for more details.</p></li>
</ul>
</li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.private_key">
<code class="sig-name descname">private_key</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.private_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The certificate’s PEM-formatted private key</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.status">
<code class="sig-name descname">status</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.status" title="Permalink to this definition">¶</a></dt>
<dd><p>Status of the certificate.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.subject_alternative_names">
<code class="sig-name descname">subject_alternative_names</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.subject_alternative_names" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of domains that should be SANs in the issued certificate. To remove all elements of a previously configured list, set this value equal to an empty list (<code class="docutils literal notranslate"><span class="pre">[]</span></code>).</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A map of tags to assign to the resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.validation_emails">
<code class="sig-name descname">validation_emails</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.validation_emails" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of addresses that received a validation E-Mail. Only set if <code class="docutils literal notranslate"><span class="pre">EMAIL</span></code>-validation was used.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.Certificate.validation_method">
<code class="sig-name descname">validation_method</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.Certificate.validation_method" title="Permalink to this definition">¶</a></dt>
<dd><p>Which method to use for validation. <code class="docutils literal notranslate"><span class="pre">DNS</span></code> or <code class="docutils literal notranslate"><span class="pre">EMAIL</span></code> are valid, <code class="docutils literal notranslate"><span class="pre">NONE</span></code> can be used for certificates that were imported into ACM and then into state managed by this provider.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.acm.Certificate.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_authority_arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_body</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_chain</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain_validation_options</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">options</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">private_key</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">status</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">subject_alternative_names</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">validation_emails</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">validation_method</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.Certificate.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Certificate resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ARN of the certificate</p></li>
<li><p><strong>certificate_authority_arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ARN of an ACMPCA</p></li>
<li><p><strong>certificate_body</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The certificate’s PEM-formatted public key</p></li>
<li><p><strong>certificate_chain</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The certificate’s PEM-formatted chain</p></li>
</ul>
</dd>
</dl>
<div class="highlight-default notranslate"><div class="highlight"><pre><span></span><span class="o">*</span> <span class="n">Creating</span> <span class="n">a</span> <span class="n">private</span> <span class="n">CA</span> <span class="n">issued</span> <span class="n">certificate</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>domain_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – A domain name for which the certificate should be issued</p></li>
<li><p><strong>domain_validation_options</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of attributes to feed into other resources to complete certificate validation. Can have more than one element, e.g. if SANs are defined. Only set if <code class="docutils literal notranslate"><span class="pre">DNS</span></code>-validation was used.</p></li>
<li><p><strong>options</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – Configuration block used to set certificate options. Detailed below.</p></li>
</ul>
</dd>
</dl>
<div class="highlight-default notranslate"><div class="highlight"><pre><span></span><span class="o">*</span> <span class="n">Importing</span> <span class="n">an</span> <span class="n">existing</span> <span class="n">certificate</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>private_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The certificate’s PEM-formatted private key</p></li>
<li><p><strong>status</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Status of the certificate.</p></li>
<li><p><strong>subject_alternative_names</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of domains that should be SANs in the issued certificate. To remove all elements of a previously configured list, set this value equal to an empty list (<code class="docutils literal notranslate"><span class="pre">[]</span></code>).</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A map of tags to assign to the resource.</p></li>
<li><p><strong>validation_emails</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of addresses that received a validation E-Mail. Only set if <code class="docutils literal notranslate"><span class="pre">EMAIL</span></code>-validation was used.</p></li>
<li><p><strong>validation_method</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Which method to use for validation. <code class="docutils literal notranslate"><span class="pre">DNS</span></code> or <code class="docutils literal notranslate"><span class="pre">EMAIL</span></code> are valid, <code class="docutils literal notranslate"><span class="pre">NONE</span></code> can be used for certificates that were imported into ACM and then into state managed by this provider.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>domain_validation_options</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">domain_name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - A domain name for which the certificate should be issued</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceRecordName</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the DNS record to create to validate the certificate</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceRecordType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The type of DNS record to create</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceRecordValue</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The value the DNS record needs to have</p></li>
</ul>
<p>The <strong>options</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">certificateTransparencyLoggingPreference</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies whether certificate details should be added to a certificate transparency log. Valid values are <code class="docutils literal notranslate"><span class="pre">ENABLED</span></code> or <code class="docutils literal notranslate"><span class="pre">DISABLED</span></code>. See <a class="reference external" href="https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html#concept-transparency">https://docs.aws.amazon.com/acm/latest/userguide/acm-concepts.html#concept-transparency</a> for more details.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.acm.Certificate.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.Certificate.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.acm.Certificate.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.Certificate.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_aws.acm.CertificateValidation">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.acm.</code><code class="sig-name descname">CertificateValidation</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">validation_record_fqdns</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.CertificateValidation" title="Permalink to this definition">¶</a></dt>
<dd><p>This resource represents a successful validation of an ACM certificate in concert
with other resources.</p>
<p>Most commonly, this resource is used together with <code class="docutils literal notranslate"><span class="pre">route53.Record</span></code> and
<code class="docutils literal notranslate"><span class="pre">acm.Certificate</span></code> to request a DNS validated certificate,
deploy the required validation records and wait for validation to complete.</p>
<blockquote>
<div><p><strong>WARNING:</strong> This resource implements a part of the validation workflow. It does not represent a real-world entity in AWS, therefore changing or deleting this resource on its own has no immediate effect.</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">cert_certificate</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">Certificate</span><span class="p">(</span><span class="s2">&quot;certCertificate&quot;</span><span class="p">,</span>
    <span class="n">domain_name</span><span class="o">=</span><span class="s2">&quot;example.com&quot;</span><span class="p">,</span>
    <span class="n">validation_method</span><span class="o">=</span><span class="s2">&quot;DNS&quot;</span><span class="p">)</span>
<span class="n">zone</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">get_zone</span><span class="p">(</span><span class="n">name</span><span class="o">=</span><span class="s2">&quot;example.com.&quot;</span><span class="p">,</span>
    <span class="n">private_zone</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">cert_validation</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">Record</span><span class="p">(</span><span class="s2">&quot;certValidation&quot;</span><span class="p">,</span>
    <span class="n">name</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;resourceRecordName&quot;</span><span class="p">],</span>
    <span class="n">records</span><span class="o">=</span><span class="p">[</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;resourceRecordValue&quot;</span><span class="p">]],</span>
    <span class="n">ttl</span><span class="o">=</span><span class="mi">60</span><span class="p">,</span>
    <span class="nb">type</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;resourceRecordType&quot;</span><span class="p">],</span>
    <span class="n">zone_id</span><span class="o">=</span><span class="n">zone</span><span class="o">.</span><span class="n">zone_id</span><span class="p">)</span>
<span class="n">cert_certificate_validation</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">CertificateValidation</span><span class="p">(</span><span class="s2">&quot;certCertificateValidation&quot;</span><span class="p">,</span>
    <span class="n">certificate_arn</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">arn</span><span class="p">,</span>
    <span class="n">validation_record_fqdns</span><span class="o">=</span><span class="p">[</span><span class="n">cert_validation</span><span class="o">.</span><span class="n">fqdn</span><span class="p">])</span>
<span class="n">front_end</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">lb</span><span class="o">.</span><span class="n">Listener</span><span class="p">(</span><span class="s2">&quot;frontEnd&quot;</span><span class="p">,</span> <span class="n">certificate_arn</span><span class="o">=</span><span class="n">cert_certificate_validation</span><span class="o">.</span><span class="n">certificate_arn</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">cert_certificate</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">Certificate</span><span class="p">(</span><span class="s2">&quot;certCertificate&quot;</span><span class="p">,</span>
    <span class="n">domain_name</span><span class="o">=</span><span class="s2">&quot;example.com&quot;</span><span class="p">,</span>
    <span class="n">subject_alternative_names</span><span class="o">=</span><span class="p">[</span>
        <span class="s2">&quot;www.example.com&quot;</span><span class="p">,</span>
        <span class="s2">&quot;example.org&quot;</span><span class="p">,</span>
    <span class="p">],</span>
    <span class="n">validation_method</span><span class="o">=</span><span class="s2">&quot;DNS&quot;</span><span class="p">)</span>
<span class="n">zone</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">get_zone</span><span class="p">(</span><span class="n">name</span><span class="o">=</span><span class="s2">&quot;example.com.&quot;</span><span class="p">,</span>
    <span class="n">private_zone</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">zone_alt</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">get_zone</span><span class="p">(</span><span class="n">name</span><span class="o">=</span><span class="s2">&quot;example.org.&quot;</span><span class="p">,</span>
    <span class="n">private_zone</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">cert_validation</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">Record</span><span class="p">(</span><span class="s2">&quot;certValidation&quot;</span><span class="p">,</span>
    <span class="n">name</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;resourceRecordName&quot;</span><span class="p">],</span>
    <span class="n">records</span><span class="o">=</span><span class="p">[</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;resourceRecordValue&quot;</span><span class="p">]],</span>
    <span class="n">ttl</span><span class="o">=</span><span class="mi">60</span><span class="p">,</span>
    <span class="nb">type</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;resourceRecordType&quot;</span><span class="p">],</span>
    <span class="n">zone_id</span><span class="o">=</span><span class="n">zone</span><span class="o">.</span><span class="n">zone_id</span><span class="p">)</span>
<span class="n">cert_validation_alt1</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">Record</span><span class="p">(</span><span class="s2">&quot;certValidationAlt1&quot;</span><span class="p">,</span>
    <span class="n">name</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="s2">&quot;resourceRecordName&quot;</span><span class="p">],</span>
    <span class="n">records</span><span class="o">=</span><span class="p">[</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="s2">&quot;resourceRecordValue&quot;</span><span class="p">]],</span>
    <span class="n">ttl</span><span class="o">=</span><span class="mi">60</span><span class="p">,</span>
    <span class="nb">type</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="s2">&quot;resourceRecordType&quot;</span><span class="p">],</span>
    <span class="n">zone_id</span><span class="o">=</span><span class="n">zone</span><span class="o">.</span><span class="n">zone_id</span><span class="p">)</span>
<span class="n">cert_validation_alt2</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">route53</span><span class="o">.</span><span class="n">Record</span><span class="p">(</span><span class="s2">&quot;certValidationAlt2&quot;</span><span class="p">,</span>
    <span class="n">name</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="s2">&quot;resourceRecordName&quot;</span><span class="p">],</span>
    <span class="n">records</span><span class="o">=</span><span class="p">[</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="s2">&quot;resourceRecordValue&quot;</span><span class="p">]],</span>
    <span class="n">ttl</span><span class="o">=</span><span class="mi">60</span><span class="p">,</span>
    <span class="nb">type</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">domain_validation_options</span><span class="p">[</span><span class="mi">2</span><span class="p">][</span><span class="s2">&quot;resourceRecordType&quot;</span><span class="p">],</span>
    <span class="n">zone_id</span><span class="o">=</span><span class="n">zone_alt</span><span class="o">.</span><span class="n">zone_id</span><span class="p">)</span>
<span class="n">cert_certificate_validation</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">CertificateValidation</span><span class="p">(</span><span class="s2">&quot;certCertificateValidation&quot;</span><span class="p">,</span>
    <span class="n">certificate_arn</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">arn</span><span class="p">,</span>
    <span class="n">validation_record_fqdns</span><span class="o">=</span><span class="p">[</span>
        <span class="n">cert_validation</span><span class="o">.</span><span class="n">fqdn</span><span class="p">,</span>
        <span class="n">cert_validation_alt1</span><span class="o">.</span><span class="n">fqdn</span><span class="p">,</span>
        <span class="n">cert_validation_alt2</span><span class="o">.</span><span class="n">fqdn</span><span class="p">,</span>
    <span class="p">])</span>
<span class="n">front_end</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">lb</span><span class="o">.</span><span class="n">Listener</span><span class="p">(</span><span class="s2">&quot;frontEnd&quot;</span><span class="p">,</span> <span class="n">certificate_arn</span><span class="o">=</span><span class="n">cert_certificate_validation</span><span class="o">.</span><span class="n">certificate_arn</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">cert_certificate</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">Certificate</span><span class="p">(</span><span class="s2">&quot;certCertificate&quot;</span><span class="p">,</span>
    <span class="n">domain_name</span><span class="o">=</span><span class="s2">&quot;example.com&quot;</span><span class="p">,</span>
    <span class="n">validation_method</span><span class="o">=</span><span class="s2">&quot;EMAIL&quot;</span><span class="p">)</span>
<span class="n">cert_certificate_validation</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">CertificateValidation</span><span class="p">(</span><span class="s2">&quot;certCertificateValidation&quot;</span><span class="p">,</span> <span class="n">certificate_arn</span><span class="o">=</span><span class="n">cert_certificate</span><span class="o">.</span><span class="n">arn</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>certificate_arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ARN of the certificate that is being validated.</p></li>
<li><p><strong>validation_record_fqdns</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – List of FQDNs that implement the validation. Only valid for DNS validation method ACM certificates. If this is set, the resource can implement additional sanity checks and has an explicit dependency on the resource that is implementing the validation</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_aws.acm.CertificateValidation.certificate_arn">
<code class="sig-name descname">certificate_arn</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.CertificateValidation.certificate_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The ARN of the certificate that is being validated.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.CertificateValidation.validation_record_fqdns">
<code class="sig-name descname">validation_record_fqdns</code><em class="property">: pulumi.Output[list]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.CertificateValidation.validation_record_fqdns" title="Permalink to this definition">¶</a></dt>
<dd><p>List of FQDNs that implement the validation. Only valid for DNS validation method ACM certificates. If this is set, the resource can implement additional sanity checks and has an explicit dependency on the resource that is implementing the validation</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.acm.CertificateValidation.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">certificate_arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">validation_record_fqdns</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.CertificateValidation.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing CertificateValidation resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>certificate_arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ARN of the certificate that is being validated.</p></li>
<li><p><strong>validation_record_fqdns</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – List of FQDNs that implement the validation. Only valid for DNS validation method ACM certificates. If this is set, the resource can implement additional sanity checks and has an explicit dependency on the resource that is implementing the validation</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.acm.CertificateValidation.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.CertificateValidation.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.acm.CertificateValidation.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.CertificateValidation.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_aws.acm.GetCertificateResult">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.acm.</code><code class="sig-name descname">GetCertificateResult</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">domain</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">key_types</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">most_recent</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">statuses</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">types</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.GetCertificateResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getCertificate.</p>
<dl class="py attribute">
<dt id="pulumi_aws.acm.GetCertificateResult.arn">
<code class="sig-name descname">arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.GetCertificateResult.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>Set to the ARN of the found certificate, suitable for referencing in other resources that support ACM certificates.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.GetCertificateResult.id">
<code class="sig-name descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.GetCertificateResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.acm.GetCertificateResult.tags">
<code class="sig-name descname">tags</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.acm.GetCertificateResult.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags for the resource.</p>
</dd></dl>

</dd></dl>

<dl class="py function">
<dt id="pulumi_aws.acm.get_certificate">
<code class="sig-prename descclassname">pulumi_aws.acm.</code><code class="sig-name descname">get_certificate</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">domain</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">key_types</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">most_recent</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">statuses</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">types</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.acm.get_certificate" title="Permalink to this definition">¶</a></dt>
<dd><p>Use this data source to get the ARN of a certificate in AWS Certificate
Manager (ACM), you can reference
it by domain without having to hard code the ARNs as input.</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">example</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">acm</span><span class="o">.</span><span class="n">get_certificate</span><span class="p">(</span><span class="n">domain</span><span class="o">=</span><span class="s2">&quot;tf.example.com&quot;</span><span class="p">,</span>
    <span class="n">key_types</span><span class="o">=</span><span class="p">[</span><span class="s2">&quot;RSA_4096&quot;</span><span class="p">])</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>domain</strong> (<em>str</em>) – The domain of the certificate to look up. If no certificate is found with this name, an error will be returned.</p></li>
<li><p><strong>key_types</strong> (<em>list</em>) – A list of key algorithms to filter certificates. By default, ACM does not return all certificate types when searching. Valid values are <code class="docutils literal notranslate"><span class="pre">RSA_1024</span></code>, <code class="docutils literal notranslate"><span class="pre">RSA_2048</span></code>, <code class="docutils literal notranslate"><span class="pre">RSA_4096</span></code>, <code class="docutils literal notranslate"><span class="pre">EC_prime256v1</span></code>, <code class="docutils literal notranslate"><span class="pre">EC_secp384r1</span></code>, and <code class="docutils literal notranslate"><span class="pre">EC_secp521r1</span></code>.</p></li>
<li><p><strong>most_recent</strong> (<em>bool</em>) – If set to true, it sorts the certificates matched by previous criteria by the NotBefore field, returning only the most recent one. If set to false, it returns an error if more than one certificate is found. Defaults to false.</p></li>
<li><p><strong>statuses</strong> (<em>list</em>) – A list of statuses on which to filter the returned list. Valid values are <code class="docutils literal notranslate"><span class="pre">PENDING_VALIDATION</span></code>, <code class="docutils literal notranslate"><span class="pre">ISSUED</span></code>,
<code class="docutils literal notranslate"><span class="pre">INACTIVE</span></code>, <code class="docutils literal notranslate"><span class="pre">EXPIRED</span></code>, <code class="docutils literal notranslate"><span class="pre">VALIDATION_TIMED_OUT</span></code>, <code class="docutils literal notranslate"><span class="pre">REVOKED</span></code> and <code class="docutils literal notranslate"><span class="pre">FAILED</span></code>. If no value is specified, only certificates in the <code class="docutils literal notranslate"><span class="pre">ISSUED</span></code> state
are returned.</p></li>
<li><p><strong>tags</strong> (<em>dict</em>) – A mapping of tags for the resource.</p></li>
<li><p><strong>types</strong> (<em>list</em>) – A list of types on which to filter the returned list. Valid values are <code class="docutils literal notranslate"><span class="pre">AMAZON_ISSUED</span></code> and <code class="docutils literal notranslate"><span class="pre">IMPORTED</span></code>.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

</div>

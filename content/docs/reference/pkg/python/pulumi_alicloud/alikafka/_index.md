---
title: Module alikafka
title_tag: Module alikafka | Package pulumi_alicloud | Python SDK
linktitle: alikafka
notitle: true
---

{{< resource-docs-alert "alicloud" >}}

<div class="section" id="alikafka">
<h1>alikafka<a class="headerlink" href="#alikafka" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-alicloud">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-alicloud/issues">pulumi/pulumi-alicloud repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-alicloud/issues">terraform-providers/terraform-provider-alicloud repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_alicloud.alikafka"></span><dl class="py class">
<dt id="pulumi_alicloud.alikafka.ConsumerGroup">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_alicloud.alikafka.</code><code class="sig-name descname">ConsumerGroup</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">consumer_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an ALIKAFKA consumer group resource.</p>
<blockquote>
<div><p><strong>NOTE:</strong> Available in 1.56.0+</p>
<p><strong>NOTE:</strong>  Only the following regions support create alikafka consumer group.
[<code class="docutils literal notranslate"><span class="pre">cn-hangzhou</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-beijing</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shenzhen</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shanghai</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-qingdao</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-hongkong</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-huhehaote</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-zhangjiakou</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-south-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-5</span></code>]</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_alicloud</span> <span class="k">as</span> <span class="nn">alicloud</span>

<span class="n">config</span> <span class="o">=</span> <span class="n">pulumi</span><span class="o">.</span><span class="n">Config</span><span class="p">()</span>
<span class="n">consumer_id</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;consumerId&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">consumer_id</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">consumer_id</span> <span class="o">=</span> <span class="s2">&quot;CID-alikafkaGroupDatasourceName&quot;</span>
<span class="n">default_zones</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">get_zones</span><span class="p">(</span><span class="n">available_resource_creation</span><span class="o">=</span><span class="s2">&quot;VSwitch&quot;</span><span class="p">)</span>
<span class="n">default_network</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Network</span><span class="p">(</span><span class="s2">&quot;defaultNetwork&quot;</span><span class="p">,</span> <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/12&quot;</span><span class="p">)</span>
<span class="n">default_switch</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Switch</span><span class="p">(</span><span class="s2">&quot;defaultSwitch&quot;</span><span class="p">,</span>
    <span class="n">availability_zone</span><span class="o">=</span><span class="n">default_zones</span><span class="o">.</span><span class="n">zones</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;id&quot;</span><span class="p">],</span>
    <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/24&quot;</span><span class="p">,</span>
    <span class="n">vpc_id</span><span class="o">=</span><span class="n">default_network</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_instance</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Instance</span><span class="p">(</span><span class="s2">&quot;defaultInstance&quot;</span><span class="p">,</span>
    <span class="n">deploy_type</span><span class="o">=</span><span class="s2">&quot;5&quot;</span><span class="p">,</span>
    <span class="n">disk_size</span><span class="o">=</span><span class="s2">&quot;500&quot;</span><span class="p">,</span>
    <span class="n">disk_type</span><span class="o">=</span><span class="s2">&quot;1&quot;</span><span class="p">,</span>
    <span class="n">io_max</span><span class="o">=</span><span class="s2">&quot;20&quot;</span><span class="p">,</span>
    <span class="n">topic_quota</span><span class="o">=</span><span class="s2">&quot;50&quot;</span><span class="p">,</span>
    <span class="n">vswitch_id</span><span class="o">=</span><span class="n">default_switch</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_consumer_group</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">ConsumerGroup</span><span class="p">(</span><span class="s2">&quot;defaultConsumerGroup&quot;</span><span class="p">,</span>
    <span class="n">consumer_id</span><span class="o">=</span><span class="n">consumer_id</span><span class="p">,</span>
    <span class="n">instance_id</span><span class="o">=</span><span class="n">default_instance</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>consumer_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the consumer group. The length cannot exceed 64 characters.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the ALIKAFKA Instance that owns the groups.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.ConsumerGroup.consumer_id">
<code class="sig-name descname">consumer_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup.consumer_id" title="Permalink to this definition">¶</a></dt>
<dd><p>ID of the consumer group. The length cannot exceed 64 characters.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.ConsumerGroup.instance_id">
<code class="sig-name descname">instance_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup.instance_id" title="Permalink to this definition">¶</a></dt>
<dd><p>ID of the ALIKAFKA Instance that owns the groups.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.ConsumerGroup.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.ConsumerGroup.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">consumer_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing ConsumerGroup resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>consumer_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the consumer group. The length cannot exceed 64 characters.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the ALIKAFKA Instance that owns the groups.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.ConsumerGroup.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.ConsumerGroup.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.ConsumerGroup.translate_input_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.Instance">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_alicloud.alikafka.</code><code class="sig-name descname">Instance</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">deploy_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">disk_size</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">disk_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eip_max</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">io_max</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">paid_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">spec_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">topic_quota</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">vswitch_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an ALIKAFKA instance resource.</p>
<blockquote>
<div><p><strong>NOTE:</strong> Available in 1.59.0+</p>
<p><strong>NOTE:</strong> ALIKAFKA instance resource only support create post pay instance. Creation or modification may took about 10-40 minutes.</p>
<p><strong>NOTE:</strong> Only the following regions support create alikafka pre paid instance.
[<code class="docutils literal notranslate"><span class="pre">cn-hangzhou</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-beijing</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shenzhen</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shanghai</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-qingdao</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-hongkong</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-huhehaote</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-zhangjiakou</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-south-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-5</span></code>]</p>
<p><strong>NOTE:</strong> Only the following regions support create alikafka post paid instance.
[<code class="docutils literal notranslate"><span class="pre">cn-hangzhou</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-beijing</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shenzhen</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shanghai</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-qingdao</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-hongkong</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-huhehaote</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-zhangjiakou</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-1</span></code>]</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_alicloud</span> <span class="k">as</span> <span class="nn">alicloud</span>

<span class="n">config</span> <span class="o">=</span> <span class="n">pulumi</span><span class="o">.</span><span class="n">Config</span><span class="p">()</span>
<span class="n">instance_name</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;instanceName&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">instance_name</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">instance_name</span> <span class="o">=</span> <span class="s2">&quot;alikafkaInstanceName&quot;</span>
<span class="n">default_zones</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">get_zones</span><span class="p">(</span><span class="n">available_resource_creation</span><span class="o">=</span><span class="s2">&quot;VSwitch&quot;</span><span class="p">)</span>
<span class="n">default_network</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Network</span><span class="p">(</span><span class="s2">&quot;defaultNetwork&quot;</span><span class="p">,</span> <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/12&quot;</span><span class="p">)</span>
<span class="n">default_switch</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Switch</span><span class="p">(</span><span class="s2">&quot;defaultSwitch&quot;</span><span class="p">,</span>
    <span class="n">availability_zone</span><span class="o">=</span><span class="n">default_zones</span><span class="o">.</span><span class="n">zones</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;id&quot;</span><span class="p">],</span>
    <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/24&quot;</span><span class="p">,</span>
    <span class="n">vpc_id</span><span class="o">=</span><span class="n">default_network</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_instance</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Instance</span><span class="p">(</span><span class="s2">&quot;defaultInstance&quot;</span><span class="p">,</span>
    <span class="n">deploy_type</span><span class="o">=</span><span class="s2">&quot;4&quot;</span><span class="p">,</span>
    <span class="n">disk_size</span><span class="o">=</span><span class="s2">&quot;500&quot;</span><span class="p">,</span>
    <span class="n">disk_type</span><span class="o">=</span><span class="s2">&quot;1&quot;</span><span class="p">,</span>
    <span class="n">io_max</span><span class="o">=</span><span class="s2">&quot;20&quot;</span><span class="p">,</span>
    <span class="n">topic_quota</span><span class="o">=</span><span class="s2">&quot;50&quot;</span><span class="p">,</span>
    <span class="n">vswitch_id</span><span class="o">=</span><span class="n">default_switch</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>deploy_type</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The deploy type of the instance. Currently only support two deploy type, 4: eip/vpc instance, 5: vpc instance.</p></li>
<li><p><strong>disk_size</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The disk size of the instance. When modify this value, it only support adjust to a greater value.</p></li>
<li><p><strong>disk_type</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The disk type of the instance. 0: efficient cloud disk , 1: SSD.</p></li>
<li><p><strong>eip_max</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max bandwidth of the instance. When modify this value, it only support adjust to a greater value.</p></li>
<li><p><strong>io_max</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max value of io of the instance. When modify this value, it only support adjust to a greater value.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Name of your Kafka instance. The length should between 3 and 64 characters. If not set, will use instance id as instance name.</p></li>
<li><p><strong>paid_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The paid type of the instance. Support two type, “PrePaid”: pre paid type instance, “PostPaid”: post paid type instance. Default is PostPaid. When modify this value, it only support adjust from post pay to pre pay.</p></li>
<li><p><strong>spec_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The spec type of the instance. Support two type, “normal”: normal version instance, “professional”: professional version instance. Default is normal. When modify this value, it only support adjust from normal to professional. Note only pre paid type instance support professional specific type.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
<li><p><strong>topic_quota</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max num of topic can be create of the instance. When modify this value, it only adjust to a greater value.</p></li>
<li><p><strong>vswitch_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of attaching vswitch to instance.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.deploy_type">
<code class="sig-name descname">deploy_type</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.deploy_type" title="Permalink to this definition">¶</a></dt>
<dd><p>The deploy type of the instance. Currently only support two deploy type, 4: eip/vpc instance, 5: vpc instance.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.disk_size">
<code class="sig-name descname">disk_size</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.disk_size" title="Permalink to this definition">¶</a></dt>
<dd><p>The disk size of the instance. When modify this value, it only support adjust to a greater value.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.disk_type">
<code class="sig-name descname">disk_type</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.disk_type" title="Permalink to this definition">¶</a></dt>
<dd><p>The disk type of the instance. 0: efficient cloud disk , 1: SSD.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.eip_max">
<code class="sig-name descname">eip_max</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.eip_max" title="Permalink to this definition">¶</a></dt>
<dd><p>The max bandwidth of the instance. When modify this value, it only support adjust to a greater value.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.io_max">
<code class="sig-name descname">io_max</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.io_max" title="Permalink to this definition">¶</a></dt>
<dd><p>The max value of io of the instance. When modify this value, it only support adjust to a greater value.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Name of your Kafka instance. The length should between 3 and 64 characters. If not set, will use instance id as instance name.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.paid_type">
<code class="sig-name descname">paid_type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.paid_type" title="Permalink to this definition">¶</a></dt>
<dd><p>The paid type of the instance. Support two type, “PrePaid”: pre paid type instance, “PostPaid”: post paid type instance. Default is PostPaid. When modify this value, it only support adjust from post pay to pre pay.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.spec_type">
<code class="sig-name descname">spec_type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.spec_type" title="Permalink to this definition">¶</a></dt>
<dd><p>The spec type of the instance. Support two type, “normal”: normal version instance, “professional”: professional version instance. Default is normal. When modify this value, it only support adjust from normal to professional. Note only pre paid type instance support professional specific type.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.topic_quota">
<code class="sig-name descname">topic_quota</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.topic_quota" title="Permalink to this definition">¶</a></dt>
<dd><p>The max num of topic can be create of the instance. When modify this value, it only adjust to a greater value.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.vpc_id">
<code class="sig-name descname">vpc_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.vpc_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of attaching VPC to instance.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.vswitch_id">
<code class="sig-name descname">vswitch_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.vswitch_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of attaching vswitch to instance.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Instance.zone_id">
<code class="sig-name descname">zone_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.zone_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The Zone to launch the kafka instance.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.Instance.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">deploy_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">disk_size</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">disk_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eip_max</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">io_max</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">paid_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">spec_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">topic_quota</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">vpc_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">vswitch_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">zone_id</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Instance resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>deploy_type</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The deploy type of the instance. Currently only support two deploy type, 4: eip/vpc instance, 5: vpc instance.</p></li>
<li><p><strong>disk_size</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The disk size of the instance. When modify this value, it only support adjust to a greater value.</p></li>
<li><p><strong>disk_type</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The disk type of the instance. 0: efficient cloud disk , 1: SSD.</p></li>
<li><p><strong>eip_max</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max bandwidth of the instance. When modify this value, it only support adjust to a greater value.</p></li>
<li><p><strong>io_max</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max value of io of the instance. When modify this value, it only support adjust to a greater value.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Name of your Kafka instance. The length should between 3 and 64 characters. If not set, will use instance id as instance name.</p></li>
<li><p><strong>paid_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The paid type of the instance. Support two type, “PrePaid”: pre paid type instance, “PostPaid”: post paid type instance. Default is PostPaid. When modify this value, it only support adjust from post pay to pre pay.</p></li>
<li><p><strong>spec_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The spec type of the instance. Support two type, “normal”: normal version instance, “professional”: professional version instance. Default is normal. When modify this value, it only support adjust from normal to professional. Note only pre paid type instance support professional specific type.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
<li><p><strong>topic_quota</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max num of topic can be create of the instance. When modify this value, it only adjust to a greater value.</p></li>
<li><p><strong>vpc_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of attaching VPC to instance.</p></li>
<li><p><strong>vswitch_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of attaching vswitch to instance.</p></li>
<li><p><strong>zone_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Zone to launch the kafka instance.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.Instance.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.Instance.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Instance.translate_input_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.SaslAcl">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_alicloud.alikafka.</code><code class="sig-name descname">SaslAcl</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_operation_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_resource_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_resource_pattern_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_resource_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">username</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an ALIKAFKA sasl acl resource.</p>
<blockquote>
<div><p><strong>NOTE:</strong> Available in 1.66.0+</p>
<p><strong>NOTE:</strong>  Only the following regions support create alikafka sasl user.
[<code class="docutils literal notranslate"><span class="pre">cn-hangzhou</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-beijing</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shenzhen</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shanghai</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-qingdao</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-hongkong</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-huhehaote</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-zhangjiakou</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-south-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-5</span></code>]</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_alicloud</span> <span class="k">as</span> <span class="nn">alicloud</span>

<span class="n">config</span> <span class="o">=</span> <span class="n">pulumi</span><span class="o">.</span><span class="n">Config</span><span class="p">()</span>
<span class="n">username</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;username&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">username</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">username</span> <span class="o">=</span> <span class="s2">&quot;testusername&quot;</span>
<span class="n">password</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;password&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">password</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">password</span> <span class="o">=</span> <span class="s2">&quot;testpassword&quot;</span>
<span class="n">default_zones</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">get_zones</span><span class="p">(</span><span class="n">available_resource_creation</span><span class="o">=</span><span class="s2">&quot;VSwitch&quot;</span><span class="p">)</span>
<span class="n">default_network</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Network</span><span class="p">(</span><span class="s2">&quot;defaultNetwork&quot;</span><span class="p">,</span> <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/12&quot;</span><span class="p">)</span>
<span class="n">default_switch</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Switch</span><span class="p">(</span><span class="s2">&quot;defaultSwitch&quot;</span><span class="p">,</span>
    <span class="n">availability_zone</span><span class="o">=</span><span class="n">default_zones</span><span class="o">.</span><span class="n">zones</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;id&quot;</span><span class="p">],</span>
    <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/24&quot;</span><span class="p">,</span>
    <span class="n">vpc_id</span><span class="o">=</span><span class="n">default_network</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_instance</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Instance</span><span class="p">(</span><span class="s2">&quot;defaultInstance&quot;</span><span class="p">,</span>
    <span class="n">deploy_type</span><span class="o">=</span><span class="s2">&quot;5&quot;</span><span class="p">,</span>
    <span class="n">disk_size</span><span class="o">=</span><span class="s2">&quot;500&quot;</span><span class="p">,</span>
    <span class="n">disk_type</span><span class="o">=</span><span class="s2">&quot;1&quot;</span><span class="p">,</span>
    <span class="n">io_max</span><span class="o">=</span><span class="s2">&quot;20&quot;</span><span class="p">,</span>
    <span class="n">topic_quota</span><span class="o">=</span><span class="s2">&quot;50&quot;</span><span class="p">,</span>
    <span class="n">vswitch_id</span><span class="o">=</span><span class="n">default_switch</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_topic</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Topic</span><span class="p">(</span><span class="s2">&quot;defaultTopic&quot;</span><span class="p">,</span>
    <span class="n">instance_id</span><span class="o">=</span><span class="n">default_instance</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
    <span class="n">remark</span><span class="o">=</span><span class="s2">&quot;topic-remark&quot;</span><span class="p">,</span>
    <span class="n">topic</span><span class="o">=</span><span class="s2">&quot;test-topic&quot;</span><span class="p">)</span>
<span class="n">default_sasl_user</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">SaslUser</span><span class="p">(</span><span class="s2">&quot;defaultSaslUser&quot;</span><span class="p">,</span>
    <span class="n">instance_id</span><span class="o">=</span><span class="n">default_instance</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
    <span class="n">password</span><span class="o">=</span><span class="n">password</span><span class="p">,</span>
    <span class="n">username</span><span class="o">=</span><span class="n">username</span><span class="p">)</span>
<span class="n">default_sasl_acl</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">SaslAcl</span><span class="p">(</span><span class="s2">&quot;defaultSaslAcl&quot;</span><span class="p">,</span>
    <span class="n">acl_operation_type</span><span class="o">=</span><span class="s2">&quot;Write&quot;</span><span class="p">,</span>
    <span class="n">acl_resource_name</span><span class="o">=</span><span class="n">default_topic</span><span class="o">.</span><span class="n">topic</span><span class="p">,</span>
    <span class="n">acl_resource_pattern_type</span><span class="o">=</span><span class="s2">&quot;LITERAL&quot;</span><span class="p">,</span>
    <span class="n">acl_resource_type</span><span class="o">=</span><span class="s2">&quot;Topic&quot;</span><span class="p">,</span>
    <span class="n">instance_id</span><span class="o">=</span><span class="n">default_instance</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
    <span class="n">username</span><span class="o">=</span><span class="n">default_sasl_user</span><span class="o">.</span><span class="n">username</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>acl_operation_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Operation type for this acl. The operation type can only be “Write” and “Read”.</p></li>
<li><p><strong>acl_resource_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Resource name for this acl. The resource name should be a topic or consumer group name.</p></li>
<li><p><strong>acl_resource_pattern_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Resource pattern type for this acl. The resource pattern support two types “LITERAL” and “PREFIXED”. “LITERAL”: A literal name defines the full name of a resource. The special wildcard character “*” can be used to represent a resource with any name. “PREFIXED”: A prefixed name defines a prefix for a resource.</p></li>
<li><p><strong>acl_resource_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Resource type for this acl. The resource type can only be “Topic” and “Group”.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the ALIKAFKA Instance that owns the groups.</p></li>
<li><p><strong>username</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.acl_operation_type">
<code class="sig-name descname">acl_operation_type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.acl_operation_type" title="Permalink to this definition">¶</a></dt>
<dd><p>Operation type for this acl. The operation type can only be “Write” and “Read”.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.acl_resource_name">
<code class="sig-name descname">acl_resource_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.acl_resource_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Resource name for this acl. The resource name should be a topic or consumer group name.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.acl_resource_pattern_type">
<code class="sig-name descname">acl_resource_pattern_type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.acl_resource_pattern_type" title="Permalink to this definition">¶</a></dt>
<dd><p>Resource pattern type for this acl. The resource pattern support two types “LITERAL” and “PREFIXED”. “LITERAL”: A literal name defines the full name of a resource. The special wildcard character “*” can be used to represent a resource with any name. “PREFIXED”: A prefixed name defines a prefix for a resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.acl_resource_type">
<code class="sig-name descname">acl_resource_type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.acl_resource_type" title="Permalink to this definition">¶</a></dt>
<dd><p>Resource type for this acl. The resource type can only be “Topic” and “Group”.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.host">
<code class="sig-name descname">host</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.host" title="Permalink to this definition">¶</a></dt>
<dd><p>The host of the acl.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.instance_id">
<code class="sig-name descname">instance_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.instance_id" title="Permalink to this definition">¶</a></dt>
<dd><p>ID of the ALIKAFKA Instance that owns the groups.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslAcl.username">
<code class="sig-name descname">username</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.username" title="Permalink to this definition">¶</a></dt>
<dd><p>Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.SaslAcl.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_operation_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_resource_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_resource_pattern_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">acl_resource_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">host</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">username</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing SaslAcl resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>acl_operation_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Operation type for this acl. The operation type can only be “Write” and “Read”.</p></li>
<li><p><strong>acl_resource_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Resource name for this acl. The resource name should be a topic or consumer group name.</p></li>
<li><p><strong>acl_resource_pattern_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Resource pattern type for this acl. The resource pattern support two types “LITERAL” and “PREFIXED”. “LITERAL”: A literal name defines the full name of a resource. The special wildcard character “*” can be used to represent a resource with any name. “PREFIXED”: A prefixed name defines a prefix for a resource.</p></li>
<li><p><strong>acl_resource_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Resource type for this acl. The resource type can only be “Topic” and “Group”.</p></li>
<li><p><strong>host</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The host of the acl.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the ALIKAFKA Instance that owns the groups.</p></li>
<li><p><strong>username</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.SaslAcl.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.SaslAcl.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslAcl.translate_input_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.SaslUser">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_alicloud.alikafka.</code><code class="sig-name descname">SaslUser</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">kms_encrypted_password</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">kms_encryption_context</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">password</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">username</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an ALIKAFKA sasl user resource.</p>
<blockquote>
<div><p><strong>NOTE:</strong> Available in 1.66.0+</p>
<p><strong>NOTE:</strong>  Only the following regions support create alikafka sasl user.
[<code class="docutils literal notranslate"><span class="pre">cn-hangzhou</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-beijing</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shenzhen</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shanghai</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-qingdao</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-hongkong</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-huhehaote</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-zhangjiakou</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-south-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-5</span></code>]</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_alicloud</span> <span class="k">as</span> <span class="nn">alicloud</span>

<span class="n">config</span> <span class="o">=</span> <span class="n">pulumi</span><span class="o">.</span><span class="n">Config</span><span class="p">()</span>
<span class="n">username</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;username&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">username</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">username</span> <span class="o">=</span> <span class="s2">&quot;testusername&quot;</span>
<span class="n">password</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;password&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">password</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">password</span> <span class="o">=</span> <span class="s2">&quot;testpassword&quot;</span>
<span class="n">default_zones</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">get_zones</span><span class="p">(</span><span class="n">available_resource_creation</span><span class="o">=</span><span class="s2">&quot;VSwitch&quot;</span><span class="p">)</span>
<span class="n">default_network</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Network</span><span class="p">(</span><span class="s2">&quot;defaultNetwork&quot;</span><span class="p">,</span> <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/12&quot;</span><span class="p">)</span>
<span class="n">default_switch</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Switch</span><span class="p">(</span><span class="s2">&quot;defaultSwitch&quot;</span><span class="p">,</span>
    <span class="n">availability_zone</span><span class="o">=</span><span class="n">default_zones</span><span class="o">.</span><span class="n">zones</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;id&quot;</span><span class="p">],</span>
    <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/24&quot;</span><span class="p">,</span>
    <span class="n">vpc_id</span><span class="o">=</span><span class="n">default_network</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_instance</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Instance</span><span class="p">(</span><span class="s2">&quot;defaultInstance&quot;</span><span class="p">,</span>
    <span class="n">deploy_type</span><span class="o">=</span><span class="s2">&quot;5&quot;</span><span class="p">,</span>
    <span class="n">disk_size</span><span class="o">=</span><span class="s2">&quot;500&quot;</span><span class="p">,</span>
    <span class="n">disk_type</span><span class="o">=</span><span class="s2">&quot;1&quot;</span><span class="p">,</span>
    <span class="n">io_max</span><span class="o">=</span><span class="s2">&quot;20&quot;</span><span class="p">,</span>
    <span class="n">topic_quota</span><span class="o">=</span><span class="s2">&quot;50&quot;</span><span class="p">,</span>
    <span class="n">vswitch_id</span><span class="o">=</span><span class="n">default_switch</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_sasl_user</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">SaslUser</span><span class="p">(</span><span class="s2">&quot;defaultSaslUser&quot;</span><span class="p">,</span>
    <span class="n">instance_id</span><span class="o">=</span><span class="n">default_instance</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
    <span class="n">password</span><span class="o">=</span><span class="n">password</span><span class="p">,</span>
    <span class="n">username</span><span class="o">=</span><span class="n">username</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the ALIKAFKA Instance that owns the groups.</p></li>
<li><p><strong>kms_encrypted_password</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – An KMS encrypts password used to a db account. You have to specify one of <code class="docutils literal notranslate"><span class="pre">password</span></code> and <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> fields.</p></li>
<li><p><strong>kms_encryption_context</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – An KMS encryption context used to decrypt <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> before creating or updating a user with <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code>. See <a class="reference external" href="https://www.alibabacloud.com/help/doc-detail/42975.htm">Encryption Context</a>. It is valid when <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> is set.</p></li>
<li><p><strong>password</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Operation password. It may consist of letters, digits, or underlines, with a length of 1 to 64 characters. You have to specify one of <code class="docutils literal notranslate"><span class="pre">password</span></code> and <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> fields.</p></li>
<li><p><strong>username</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Username for the sasl user. The length should between 1 to 64 characters. The characters can only contain ‘a’-‘z’, ‘A’-‘Z’, ‘0’-‘9’, ‘_’ and ‘-‘.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslUser.instance_id">
<code class="sig-name descname">instance_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.instance_id" title="Permalink to this definition">¶</a></dt>
<dd><p>ID of the ALIKAFKA Instance that owns the groups.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslUser.kms_encrypted_password">
<code class="sig-name descname">kms_encrypted_password</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.kms_encrypted_password" title="Permalink to this definition">¶</a></dt>
<dd><p>An KMS encrypts password used to a db account. You have to specify one of <code class="docutils literal notranslate"><span class="pre">password</span></code> and <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> fields.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslUser.kms_encryption_context">
<code class="sig-name descname">kms_encryption_context</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.kms_encryption_context" title="Permalink to this definition">¶</a></dt>
<dd><p>An KMS encryption context used to decrypt <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> before creating or updating a user with <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code>. See <a class="reference external" href="https://www.alibabacloud.com/help/doc-detail/42975.htm">Encryption Context</a>. It is valid when <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> is set.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslUser.password">
<code class="sig-name descname">password</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.password" title="Permalink to this definition">¶</a></dt>
<dd><p>Operation password. It may consist of letters, digits, or underlines, with a length of 1 to 64 characters. You have to specify one of <code class="docutils literal notranslate"><span class="pre">password</span></code> and <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> fields.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.SaslUser.username">
<code class="sig-name descname">username</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.username" title="Permalink to this definition">¶</a></dt>
<dd><p>Username for the sasl user. The length should between 1 to 64 characters. The characters can only contain ‘a’-‘z’, ‘A’-‘Z’, ‘0’-‘9’, ‘_’ and ‘-‘.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.SaslUser.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">kms_encrypted_password</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">kms_encryption_context</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">password</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">username</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing SaslUser resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – ID of the ALIKAFKA Instance that owns the groups.</p></li>
<li><p><strong>kms_encrypted_password</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – An KMS encrypts password used to a db account. You have to specify one of <code class="docutils literal notranslate"><span class="pre">password</span></code> and <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> fields.</p></li>
<li><p><strong>kms_encryption_context</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – <p>An KMS encryption context used to decrypt <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> before creating or updating a user with <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code>. See <a class="reference external" href="https://www.alibabacloud.com/help/doc-detail/42975.htm">Encryption Context</a>. It is valid when <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> is set.</p>
</p></li>
<li><p><strong>password</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Operation password. It may consist of letters, digits, or underlines, with a length of 1 to 64 characters. You have to specify one of <code class="docutils literal notranslate"><span class="pre">password</span></code> and <code class="docutils literal notranslate"><span class="pre">kms_encrypted_password</span></code> fields.</p></li>
<li><p><strong>username</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Username for the sasl user. The length should between 1 to 64 characters. The characters can only contain ‘a’-‘z’, ‘A’-‘Z’, ‘0’-‘9’, ‘_’ and ‘-‘.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.SaslUser.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.SaslUser.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.SaslUser.translate_input_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.Topic">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_alicloud.alikafka.</code><code class="sig-name descname">Topic</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">compact_topic</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">local_topic</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">partition_num</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">remark</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">topic</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an ALIKAFKA topic resource.</p>
<blockquote>
<div><p><strong>NOTE:</strong> Available in 1.56.0+</p>
<p><strong>NOTE:</strong>  Only the following regions support create alikafka topic.
[<code class="docutils literal notranslate"><span class="pre">cn-hangzhou</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-beijing</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shenzhen</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-shanghai</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-qingdao</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-hongkong</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-huhehaote</span></code>,<code class="docutils literal notranslate"><span class="pre">cn-zhangjiakou</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-south-1</span></code>,<code class="docutils literal notranslate"><span class="pre">ap-southeast-5</span></code>]</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_alicloud</span> <span class="k">as</span> <span class="nn">alicloud</span>

<span class="n">default_zones</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">get_zones</span><span class="p">(</span><span class="n">available_resource_creation</span><span class="o">=</span><span class="s2">&quot;VSwitch&quot;</span><span class="p">)</span>
<span class="n">default_network</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Network</span><span class="p">(</span><span class="s2">&quot;defaultNetwork&quot;</span><span class="p">,</span> <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/12&quot;</span><span class="p">)</span>
<span class="n">default_switch</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">vpc</span><span class="o">.</span><span class="n">Switch</span><span class="p">(</span><span class="s2">&quot;defaultSwitch&quot;</span><span class="p">,</span>
    <span class="n">availability_zone</span><span class="o">=</span><span class="n">default_zones</span><span class="o">.</span><span class="n">zones</span><span class="p">[</span><span class="mi">0</span><span class="p">][</span><span class="s2">&quot;id&quot;</span><span class="p">],</span>
    <span class="n">cidr_block</span><span class="o">=</span><span class="s2">&quot;172.16.0.0/24&quot;</span><span class="p">,</span>
    <span class="n">vpc_id</span><span class="o">=</span><span class="n">default_network</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">default_instance</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Instance</span><span class="p">(</span><span class="s2">&quot;defaultInstance&quot;</span><span class="p">,</span>
    <span class="n">deploy_type</span><span class="o">=</span><span class="s2">&quot;5&quot;</span><span class="p">,</span>
    <span class="n">disk_size</span><span class="o">=</span><span class="s2">&quot;500&quot;</span><span class="p">,</span>
    <span class="n">disk_type</span><span class="o">=</span><span class="s2">&quot;1&quot;</span><span class="p">,</span>
    <span class="n">io_max</span><span class="o">=</span><span class="s2">&quot;20&quot;</span><span class="p">,</span>
    <span class="n">topic_quota</span><span class="o">=</span><span class="s2">&quot;50&quot;</span><span class="p">,</span>
    <span class="n">vswitch_id</span><span class="o">=</span><span class="n">default_switch</span><span class="o">.</span><span class="n">id</span><span class="p">)</span>
<span class="n">config</span> <span class="o">=</span> <span class="n">pulumi</span><span class="o">.</span><span class="n">Config</span><span class="p">()</span>
<span class="n">topic</span> <span class="o">=</span> <span class="n">config</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;topic&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">topic</span> <span class="ow">is</span> <span class="kc">None</span><span class="p">:</span>
    <span class="n">topic</span> <span class="o">=</span> <span class="s2">&quot;alikafkaTopicName&quot;</span>
<span class="n">default_topic</span> <span class="o">=</span> <span class="n">alicloud</span><span class="o">.</span><span class="n">alikafka</span><span class="o">.</span><span class="n">Topic</span><span class="p">(</span><span class="s2">&quot;defaultTopic&quot;</span><span class="p">,</span>
    <span class="n">compact_topic</span><span class="o">=</span><span class="s2">&quot;false&quot;</span><span class="p">,</span>
    <span class="n">instance_id</span><span class="o">=</span><span class="n">default_instance</span><span class="o">.</span><span class="n">id</span><span class="p">,</span>
    <span class="n">local_topic</span><span class="o">=</span><span class="s2">&quot;false&quot;</span><span class="p">,</span>
    <span class="n">partition_num</span><span class="o">=</span><span class="s2">&quot;12&quot;</span><span class="p">,</span>
    <span class="n">remark</span><span class="o">=</span><span class="s2">&quot;dafault_kafka_topic_remark&quot;</span><span class="p">,</span>
    <span class="n">topic</span><span class="o">=</span><span class="n">topic</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>compact_topic</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Whether the topic is compactTopic or not. Compact topic must be a localTopic.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – InstanceId of your Kafka resource, the topic will create in this instance.</p></li>
<li><p><strong>local_topic</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Whether the topic is localTopic or not.</p></li>
<li><p><strong>partition_num</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The number of partitions of the topic. The number should between 1 and 48.</p></li>
<li><p><strong>remark</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – This attribute is a concise description of topic. The length cannot exceed 64.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
<li><p><strong>topic</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Name of the topic. Two topics on a single instance cannot have the same name. The length cannot exceed 64 characters.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.compact_topic">
<code class="sig-name descname">compact_topic</code><em class="property">: pulumi.Output[bool]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.compact_topic" title="Permalink to this definition">¶</a></dt>
<dd><p>Whether the topic is compactTopic or not. Compact topic must be a localTopic.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.instance_id">
<code class="sig-name descname">instance_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.instance_id" title="Permalink to this definition">¶</a></dt>
<dd><p>InstanceId of your Kafka resource, the topic will create in this instance.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.local_topic">
<code class="sig-name descname">local_topic</code><em class="property">: pulumi.Output[bool]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.local_topic" title="Permalink to this definition">¶</a></dt>
<dd><p>Whether the topic is localTopic or not.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.partition_num">
<code class="sig-name descname">partition_num</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.partition_num" title="Permalink to this definition">¶</a></dt>
<dd><p>The number of partitions of the topic. The number should between 1 and 48.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.remark">
<code class="sig-name descname">remark</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.remark" title="Permalink to this definition">¶</a></dt>
<dd><p>This attribute is a concise description of topic. The length cannot exceed 64.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_alicloud.alikafka.Topic.topic">
<code class="sig-name descname">topic</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.topic" title="Permalink to this definition">¶</a></dt>
<dd><p>Name of the topic. Two topics on a single instance cannot have the same name. The length cannot exceed 64 characters.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.Topic.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">compact_topic</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">instance_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">local_topic</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">partition_num</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">remark</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">topic</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Topic resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>compact_topic</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Whether the topic is compactTopic or not. Compact topic must be a localTopic.</p></li>
<li><p><strong>instance_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – InstanceId of your Kafka resource, the topic will create in this instance.</p></li>
<li><p><strong>local_topic</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Whether the topic is localTopic or not.</p></li>
<li><p><strong>partition_num</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The number of partitions of the topic. The number should between 1 and 48.</p></li>
<li><p><strong>remark</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – This attribute is a concise description of topic. The length cannot exceed 64.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
<li><p><strong>topic</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Name of the topic. Two topics on a single instance cannot have the same name. The length cannot exceed 64 characters.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_alicloud.alikafka.Topic.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.translate_output_property" title="Permalink to this definition">¶</a></dt>
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
<dt id="pulumi_alicloud.alikafka.Topic.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_alicloud.alikafka.Topic.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

</div>

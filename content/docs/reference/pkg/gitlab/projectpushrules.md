
---
title: "ProjectPushRules"
block_external_search_index: true
---



This resource allows you to create and manage push rules for your GitLab projects.
For further information on push rules, consult the [gitlab
documentation](https://docs.gitlab.com/ce/push_rules/push_rules.html#push-rules).

> This content is derived from https://github.com/terraform-providers/terraform-provider-gitlab/blob/master/website/docs/r/project_push_rules.html.markdown.



## Create a ProjectPushRules Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gitlab/#ProjectPushRules">ProjectPushRules</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gitlab/#ProjectPushRulesArgs">ProjectPushRulesArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">ProjectPushRules</span><span class="p">(resource_name, opts=None, </span>author_email_regex=None<span class="p">, </span>branch_name_regex=None<span class="p">, </span>commit_message_regex=None<span class="p">, </span>deny_delete_tag=None<span class="p">, </span>file_name_regex=None<span class="p">, </span>max_file_size=None<span class="p">, </span>member_check=None<span class="p">, </span>prevent_secrets=None<span class="p">, </span>project=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewProjectPushRules<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gitlab/sdk/go/gitlab/?tab=doc#ProjectPushRulesArgs">ProjectPushRulesArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gitlab/sdk/go/gitlab/?tab=doc#ProjectPushRules">ProjectPushRules</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gitlab/Pulumi.Gitlab.ProjectPushRules.html">ProjectPushRules</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gitlab/Pulumi.GitLab.ProjectPushRulesArgs.html">ProjectPushRulesArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

#### Resource Arguments




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Author<wbr>Email<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Branch<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Commit<wbr>Message<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deny<wbr>Delete<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>File<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>File<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Member<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Prevent<wbr>Secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Author<wbr>Email<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Branch<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Commit<wbr>Message<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deny<wbr>Delete<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>File<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>File<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Member<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Prevent<wbr>Secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>author<wbr>Email<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>branch<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>commit<wbr>Message<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deny<wbr>Delete<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>file<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>File<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>member<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>prevent<wbr>Secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>author_<wbr>email_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>branch_<wbr>name_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>commit_<wbr>message_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deny_<wbr>delete_<wbr>tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>file_<wbr>name_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>file_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>member_<wbr>check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>prevent_<wbr>secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Look up an Existing ProjectPushRules Resource

Get an existing ProjectPushRules resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gitlab/#ProjectPushRulesState">ProjectPushRulesState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gitlab/#ProjectPushRules">ProjectPushRules</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>author_email_regex=None<span class="p">, </span>branch_name_regex=None<span class="p">, </span>commit_message_regex=None<span class="p">, </span>deny_delete_tag=None<span class="p">, </span>file_name_regex=None<span class="p">, </span>max_file_size=None<span class="p">, </span>member_check=None<span class="p">, </span>prevent_secrets=None<span class="p">, </span>project=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetProjectPushRules<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gitlab/sdk/go/gitlab/?tab=doc#ProjectPushRulesState">ProjectPushRulesState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gitlab/sdk/go/gitlab/?tab=doc#ProjectPushRules">ProjectPushRules</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gitlab/Pulumi.Gitlab.ProjectPushRules.html">ProjectPushRules</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gitlab/Pulumi.Gitlab..ProjectPushRulesState.html">ProjectPushRulesState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Author<wbr>Email<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Branch<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Commit<wbr>Message<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deny<wbr>Delete<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>File<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>File<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Member<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Prevent<wbr>Secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Author<wbr>Email<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Branch<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Commit<wbr>Message<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Deny<wbr>Delete<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>File<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>File<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Member<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Prevent<wbr>Secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>author<wbr>Email<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>branch<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>commit<wbr>Message<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deny<wbr>Delete<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>file<wbr>Name<wbr>Regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>File<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>member<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>prevent<wbr>Secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>author_<wbr>email_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All commit author emails must match this regex, e.g. "@my-company.com$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>branch_<wbr>name_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All branch names must match this regex, e.g. "(feature|hotfix)\/*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>commit_<wbr>message_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All commit messages must match this regex, e.g. "Fixed \d+\..*"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>deny_<wbr>delete_<wbr>tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Deny deleting a tag
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>file_<wbr>name_<wbr>regex</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}All commited filenames must not match this regex, e.g. "(jar|exe)$"
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>file_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Maximum file size (MB)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>member_<wbr>check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Restrict commits by author (email) to existing GitLab users
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>prevent_<wbr>secrets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}GitLab will reject any files that are likely to contain secrets
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name or id of the project to add the push rules to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-gitlab">https://github.com/pulumi/pulumi-gitlab</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>


---
title: "Instance"
block_external_search_index: true
---



Provides a Elasticsearch instance resource. It contains data nodes, dedicated master node(optional) and etc. It can be associated with private IP whitelists and kibana IP whitelist.

> **NOTE:** Only one operation is supported in a request. So if `data_node_spec` and `data_node_disk_size` are both changed, system will respond error.

> **NOTE:** At present, `version` can not be modified once instance has been created.

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/r/elasticsearch.html.markdown.



## Create a Instance Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/elasticsearch/#Instance">Instance</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/elasticsearch/#InstanceArgs">InstanceArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Instance</span><span class="p">(resource_name, opts=None, </span>data_node_amount=None<span class="p">, </span>data_node_disk_size=None<span class="p">, </span>data_node_disk_type=None<span class="p">, </span>data_node_spec=None<span class="p">, </span>description=None<span class="p">, </span>instance_charge_type=None<span class="p">, </span>kibana_whitelists=None<span class="p">, </span>kms_encrypted_password=None<span class="p">, </span>kms_encryption_context=None<span class="p">, </span>master_node_spec=None<span class="p">, </span>password=None<span class="p">, </span>period=None<span class="p">, </span>private_whitelists=None<span class="p">, </span>public_whitelists=None<span class="p">, </span>tags=None<span class="p">, </span>version=None<span class="p">, </span>vswitch_id=None<span class="p">, </span>zone_count=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewInstance<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/elasticsearch?tab=doc#InstanceArgs">InstanceArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/elasticsearch?tab=doc#Instance">Instance</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.ElasticSearch.Instance.html">Instance</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.AliCloud.ElasticSearch.InstanceArgs.html">InstanceArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Data<wbr>Node<wbr>Amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Charge<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encrypted<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encryption<wbr>Context</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Public<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Data<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Charge<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encrypted<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encryption<wbr>Context</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Public<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>data<wbr>Node<wbr>Amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>data<wbr>Node<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>data<wbr>Node<wbr>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>data<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Charge<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms<wbr>Encrypted<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms<wbr>Encryption<wbr>Context</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>public<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>data_<wbr>node_<wbr>amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>data_<wbr>node_<wbr>disk_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>data_<wbr>node_<wbr>disk_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>data_<wbr>node_<wbr>spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>vswitch_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>charge_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana_<wbr>whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms_<wbr>encrypted_<wbr>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms_<wbr>encryption_<wbr>context</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master_<wbr>node_<wbr>spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private_<wbr>whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>public_<wbr>whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Instance Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kibana<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kibana<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kibana<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kibana<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kibana<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kibana<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kibana_<wbr>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kibana_<wbr>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Instance Resource

Get an existing Instance resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/elasticsearch/#InstanceState">InstanceState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/elasticsearch/#Instance">Instance</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>data_node_amount=None<span class="p">, </span>data_node_disk_size=None<span class="p">, </span>data_node_disk_type=None<span class="p">, </span>data_node_spec=None<span class="p">, </span>description=None<span class="p">, </span>domain=None<span class="p">, </span>instance_charge_type=None<span class="p">, </span>kibana_domain=None<span class="p">, </span>kibana_port=None<span class="p">, </span>kibana_whitelists=None<span class="p">, </span>kms_encrypted_password=None<span class="p">, </span>kms_encryption_context=None<span class="p">, </span>master_node_spec=None<span class="p">, </span>password=None<span class="p">, </span>period=None<span class="p">, </span>port=None<span class="p">, </span>private_whitelists=None<span class="p">, </span>public_whitelists=None<span class="p">, </span>status=None<span class="p">, </span>tags=None<span class="p">, </span>version=None<span class="p">, </span>vswitch_id=None<span class="p">, </span>zone_count=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetInstance<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/elasticsearch?tab=doc#InstanceState">InstanceState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/elasticsearch?tab=doc#Instance">Instance</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.ElasticSearch.Instance.html">Instance</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.ElasticSearch.InstanceState.html">InstanceState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Data<wbr>Node<wbr>Amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Charge<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encrypted<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encryption<wbr>Context</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Public<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Data<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Charge<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kibana<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encrypted<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kms<wbr>Encryption<wbr>Context</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Public<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>data<wbr>Node<wbr>Amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>data<wbr>Node<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>data<wbr>Node<wbr>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>data<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Charge<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms<wbr>Encrypted<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms<wbr>Encryption<wbr>Context</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master<wbr>Node<wbr>Spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>public<wbr>Whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>data_<wbr>node_<wbr>amount</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch cluster's data node quantity, between 2 and 50.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>data_<wbr>node_<wbr>disk_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The single data node storage space.
- `cloud_ssd`: An SSD disk, supports a maximum of 2048 GiB (2 TB).
- `cloud_efficiency` An ultra disk, supports a maximum of 5120 GiB (5 TB). If the data to be stored is larger than 2048 GiB, an ultra disk can only support the following data sizes (GiB): [`2560`, `3072`, `3584`, `4096`, `4608`, `5120`].
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>data_<wbr>node_<wbr>disk_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data node disk type. Supported values: cloud_ssd, cloud_efficiency.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>data_<wbr>node_<wbr>spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data node specifications of the Elasticsearch instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of instance. It a string of 0 to 30 characters.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Instance connection domain (only VPC network access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>charge_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Valid values are `PrePaid`, `PostPaid`, Default to `PostPaid`. From version 1.69.0, the Elasticsearch cluster allows you to update your instance_charge_ype from `PostPaid` to `PrePaid`, the following attributes are required: `period`. But, updating from `PostPaid` to `PrePaid` is not supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana_<wbr>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Kibana console domain (Internet access supported).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana_<wbr>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Kibana console port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kibana_<wbr>whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Set the Kibana's IP whitelist in internet network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms_<wbr>encrypted_<wbr>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An KMS encrypts password used to a instance. If the `password` is filled in, this field will be ignored, but you have to specify one of `password` and `kms_encrypted_password` fields.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kms_<wbr>encryption_<wbr>context</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}An KMS encryption context used to decrypt `kms_encrypted_password` before creating or updating instance with `kms_encrypted_password`. See [Encryption Context](https://www.alibabacloud.com/help/doc-detail/42975.htm). It is valid when `kms_encrypted_password` is set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master_<wbr>node_<wbr>spec</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The dedicated master node spec. If specified, dedicated master node will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of the instance. The password can be 8 to 30 characters in length and must contain three of the following conditions: uppercase letters, lowercase letters, numbers, and special characters (`!@#$%^&*()_+-=`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The duration that you will buy Elasticsearch instance (in month). It is valid when instance_charge_type is `PrePaid`. Valid values: [1~9], 12, 24, 36. Default to 1. From version 1.69.2, when to modify this value, the resource can renewal a `PrePaid` instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Instance connection port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private_<wbr>whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Set the instance's IP whitelist in VPC network.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>public_<wbr>whitelists</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Elasticsearch instance status. Includes `active`, `activating`, `inactive`. Some operations are denied when status is not `active`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource. 
- key: It can be up to 128 characters in length. It cannot begin with "aliyun", "acs:". It cannot contain "http://" and "https://". It cannot be a null string.
- value: It can be up to 128 characters in length. It cannot contain "http://" and "https://". It can be a null string.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Elasticsearch version. Supported values: `5.5.3_with_X-Pack`, `6.3_with_X-Pack` and `6.7_with_X-Pack`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vswitch_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of VSwitch.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The Multi-AZ supported for Elasticsearch, between 1 and 3. The `data_node_amount` value must be an integral multiple of the `zone_count` value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

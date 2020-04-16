
---
title: "Dashboard"
block_external_search_index: true
---






## Create a Dashboard Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/signalfx/#Dashboard">Dashboard</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/signalfx/#DashboardArgs">DashboardArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Dashboard</span><span class="p">(resource_name, opts=None, </span>authorized_writer_teams=None<span class="p">, </span>authorized_writer_users=None<span class="p">, </span>charts=None<span class="p">, </span>charts_resolution=None<span class="p">, </span>columns=None<span class="p">, </span>dashboard_group=None<span class="p">, </span>description=None<span class="p">, </span>discovery_options_query=None<span class="p">, </span>discovery_options_selectors=None<span class="p">, </span>end_time=None<span class="p">, </span>event_overlays=None<span class="p">, </span>filters=None<span class="p">, </span>grids=None<span class="p">, </span>name=None<span class="p">, </span>selected_event_overlays=None<span class="p">, </span>start_time=None<span class="p">, </span>time_range=None<span class="p">, </span>variables=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewDashboard<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardArgs">DashboardArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#Dashboard">Dashboard</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Signalfx/Pulumi.Signalfx.Dashboard.html">Dashboard</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Signalfx/Pulumi.SignalFx.DashboardArgs.html">DashboardArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Dashboard<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Users</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Chart<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts<wbr>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Column<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>End<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Event<wbr>Overlay<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Filter<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Grid<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Selected<wbr>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Time<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Variable<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Dashboard<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Users</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">[]Dashboard<wbr>Chart</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts<wbr>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">[]Dashboard<wbr>Column</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>End<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">[]Dashboard<wbr>Event<wbr>Overlay</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">[]Dashboard<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">[]Dashboard<wbr>Grid</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Selected<wbr>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">[]Dashboard<wbr>Selected<wbr>Event<wbr>Overlay</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Time<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">[]Dashboard<wbr>Variable</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>dashboard<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorized<wbr>Writer<wbr>Teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorized<wbr>Writer<wbr>Users</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">Dashboard<wbr>Chart[]</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts<wbr>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">Dashboard<wbr>Column[]</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery<wbr>Options<wbr>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery<wbr>Options<wbr>Selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>end<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">Dashboard<wbr>Event<wbr>Overlay[]</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">Dashboard<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">Dashboard<wbr>Grid[]</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>selected<wbr>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">Dashboard<wbr>Selected<wbr>Event<wbr>Overlay[]</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>time<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">Dashboard<wbr>Variable[]</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>dashboard_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorized_<wbr>writer_<wbr>teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorized_<wbr>writer_<wbr>users</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">List[Dashboard<wbr>Chart]</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts_<wbr>resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">List[Dashboard<wbr>Column]</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery_<wbr>options_<wbr>query</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery_<wbr>options_<wbr>selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>end_<wbr>time</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>event_<wbr>overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">List[Dashboard<wbr>Event<wbr>Overlay]</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">List[Dashboard<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">List[Dashboard<wbr>Grid]</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>selected_<wbr>event_<wbr>overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">List[Dashboard<wbr>Selected<wbr>Event<wbr>Overlay]</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>start_<wbr>time</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>time_<wbr>range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">List[Dashboard<wbr>Variable]</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Dashboard Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Dashboard Resource

Get an existing Dashboard resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/signalfx/#DashboardState">DashboardState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/signalfx/#Dashboard">Dashboard</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>authorized_writer_teams=None<span class="p">, </span>authorized_writer_users=None<span class="p">, </span>charts=None<span class="p">, </span>charts_resolution=None<span class="p">, </span>columns=None<span class="p">, </span>dashboard_group=None<span class="p">, </span>description=None<span class="p">, </span>discovery_options_query=None<span class="p">, </span>discovery_options_selectors=None<span class="p">, </span>end_time=None<span class="p">, </span>event_overlays=None<span class="p">, </span>filters=None<span class="p">, </span>grids=None<span class="p">, </span>name=None<span class="p">, </span>selected_event_overlays=None<span class="p">, </span>start_time=None<span class="p">, </span>time_range=None<span class="p">, </span>url=None<span class="p">, </span>variables=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetDashboard<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardState">DashboardState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#Dashboard">Dashboard</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Signalfx/Pulumi.Signalfx.Dashboard.html">Dashboard</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Signalfx/Pulumi.Signalfx..DashboardState.html">DashboardState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Authorized<wbr>Writer<wbr>Teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Users</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Chart<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts<wbr>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Column<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dashboard<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>End<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Event<wbr>Overlay<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Filter<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Grid<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Selected<wbr>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Time<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Variable<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorized<wbr>Writer<wbr>Users</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">[]Dashboard<wbr>Chart</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Charts<wbr>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">[]Dashboard<wbr>Column</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dashboard<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Discovery<wbr>Options<wbr>Selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>End<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">[]Dashboard<wbr>Event<wbr>Overlay</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">[]Dashboard<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">[]Dashboard<wbr>Grid</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Selected<wbr>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">[]Dashboard<wbr>Selected<wbr>Event<wbr>Overlay</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Time<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">[]Dashboard<wbr>Variable</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authorized<wbr>Writer<wbr>Teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorized<wbr>Writer<wbr>Users</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">Dashboard<wbr>Chart[]</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts<wbr>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">Dashboard<wbr>Column[]</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dashboard<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery<wbr>Options<wbr>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery<wbr>Options<wbr>Selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>end<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">Dashboard<wbr>Event<wbr>Overlay[]</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">Dashboard<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">Dashboard<wbr>Grid[]</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>selected<wbr>Event<wbr>Overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">Dashboard<wbr>Selected<wbr>Event<wbr>Overlay[]</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>start<wbr>Time</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>time<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">Dashboard<wbr>Variable[]</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authorized_<wbr>writer_<wbr>teams</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Team IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorized_<wbr>writer_<wbr>users</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}User IDs that have write access to this dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardchart">List[Dashboard<wbr>Chart]</a></span>
    </dt>
    <dd>{{% md %}}Chart ID and layout information for the charts in the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>charts_<wbr>resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the chart data display resolution for charts in this dashboard. Value can be one of `"default"`,  `"low"`, `"high"`, or  `"highest"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>columns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardcolumn">List[Dashboard<wbr>Column]</a></span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dashboard_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the dashboard group that contains the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery_<wbr>options_<wbr>query</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>discovery_<wbr>options_<wbr>selectors</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>end_<wbr>time</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>event_<wbr>overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlay">List[Dashboard<wbr>Event<wbr>Overlay]</a></span>
    </dt>
    <dd>{{% md %}}Specify a list of event overlays to include in the dashboard. Note: These overlays correspond to the *suggested* event overlays specified in the web UI, and they're not automatically applied as active overlays. To set default active event overlays, use the `selected_event_overlay` property instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardfilter">List[Dashboard<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}Filter to apply to the charts when displaying the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grids</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardgrid">List[Dashboard<wbr>Grid]</a></span>
    </dt>
    <dd>{{% md %}}Grid dashboard layout. Charts listed will be placed in a grid by row with the same width and height. If a chart cannot fit in a row, it will be placed automatically in the next row.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the dashboard.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>selected_<wbr>event_<wbr>overlays</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlay">List[Dashboard<wbr>Selected<wbr>Event<wbr>Overlay]</a></span>
    </dt>
    <dd>{{% md %}}Defines event overlays which are enabled by **default**. Any overlay specified here should have an accompanying entry in `event_overlay`, which are similar to the properties here.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>start_<wbr>time</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Seconds since epoch. Used for visualization. You must specify time_span_type = `"absolute"` too.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>time_<wbr>range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time range prior to now to visualize. SignalFx time syntax (e.g. `"-5m"`, `"-1h"`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL of the dashboard
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardvariable">List[Dashboard<wbr>Variable]</a></span>
    </dt>
    <dd>{{% md %}}Dashboard variable to apply to each chart in the dashboard.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Dashboard<wbr>Chart</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardChart">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardChart">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardChartArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardChartOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Chart<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the chart to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Column</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Row</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The row to show the chart in (zero-based); if `height > 1`, this value represents the topmost row of the chart (greater than or equal to `0`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Chart<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the chart to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Column</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Row</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The row to show the chart in (zero-based); if `height > 1`, this value represents the topmost row of the chart (greater than or equal to `0`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>chart<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the chart to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>column</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>height</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>row</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The row to show the chart in (zero-based); if `height > 1`, this value represents the topmost row of the chart (greater than or equal to `0`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>width</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>chart<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the chart to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>column</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>height</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>row</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The row to show the chart in (zero-based); if `height > 1`, this value represents the topmost row of the chart (greater than or equal to `0`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>width</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Column</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardColumn">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardColumn">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardColumnArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardColumnOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Column</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Column</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>column</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>height</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>width</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>column</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Column number for the layout.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>height</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>width</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Event<wbr>Overlay</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardEventOverlay">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardEventOverlay">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardEventOverlayArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardEventOverlayOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Color</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Color to use : gray, blue, azure, navy, brown, orange, yellow, iris, magenta, pink, purple, violet, lilac, emerald, green, aquamarine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Text shown in the dropdown when selecting this overlay from the menu.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Line</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Show a vertical line for the event. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlaysource">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Event<wbr>Overlay<wbr>Source<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Color</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Color to use : gray, blue, azure, navy, brown, orange, yellow, iris, magenta, pink, purple, violet, lilac, emerald, green, aquamarine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Text shown in the dropdown when selecting this overlay from the menu.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Line</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Show a vertical line for the event. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlaysource">[]Dashboard<wbr>Event<wbr>Overlay<wbr>Source</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>color</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Color to use : gray, blue, azure, navy, brown, orange, yellow, iris, magenta, pink, purple, violet, lilac, emerald, green, aquamarine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Text shown in the dropdown when selecting this overlay from the menu.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>line</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Show a vertical line for the event. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlaysource">Dashboard<wbr>Event<wbr>Overlay<wbr>Source[]</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>color</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Color to use : gray, blue, azure, navy, brown, orange, yellow, iris, magenta, pink, purple, violet, lilac, emerald, green, aquamarine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>label</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Text shown in the dropdown when selecting this overlay from the menu.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>line</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Show a vertical line for the event. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardeventoverlaysource">List[Dashboard<wbr>Event<wbr>Overlay<wbr>Source]</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Event<wbr>Overlay<wbr>Source</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardEventOverlaySource">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardEventOverlaySource">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardEventOverlaySourceArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardEventOverlaySourceOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Filter</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardFilter">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardFilter">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardFilterArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardFilterOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Grid</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardGrid">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardGrid">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardGridArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardGridOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>height</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>width</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>chart<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of IDs of the charts to display.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>height</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}How many rows every chart should take up (greater than or equal to 1). 1 by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>width</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}How many columns (out of a total of `12`) every chart should take up (between `1` and `12`). `12` by default.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Selected<wbr>Event<wbr>Overlay</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardSelectedEventOverlay">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardSelectedEventOverlay">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardSelectedEventOverlayArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardSelectedEventOverlayOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlaysource">List&lt;Pulumi.<wbr>Signal<wbr>Fx.<wbr>Inputs.<wbr>Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Source<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlaysource">[]Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Source</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlaysource">Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Source[]</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>signal</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Search term used to choose the events shown in the overlay.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#dashboardselectedeventoverlaysource">List[Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Source]</a></span>
    </dt>
    <dd>{{% md %}}Each element specifies a filter to use against the signal specified in the `signal`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Can be set to `eventTimeSeries` (the default) to refer to externally reported events, or `detectorEvents` to refer to events from detector triggers.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Selected<wbr>Event<wbr>Overlay<wbr>Source</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardSelectedEventOverlaySource">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardSelectedEventOverlaySource">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardSelectedEventOverlaySourceArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardSelectedEventOverlaySourceOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>negated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true,  only data that does not match the specified value of the specified property appear in the event overlay. Defaults to `false`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Dashboard<wbr>Variable</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/input/#DashboardVariable">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/signalfx/types/output/#DashboardVariable">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardVariableArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-signalfx/sdk/go/signalfx/?tab=doc#DashboardVariableOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Alias</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An alias for the dashboard variable. This text will appear as the label for the dropdown field on the dashboard.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Replace<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable will only apply to charts that have a filter for the property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Restricted<wbr>Suggestions</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable may only be set to the values listed in `values_suggested` and only these values will appear in autosuggestion menus. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a value is required for this variable (and therefore whether it will be possible to view this dashboard without this filter applied). `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Values<wbr>Suggesteds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of strings of suggested values for this variable; these suggestions will receive priority when values are autosuggested for this variable.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Alias</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An alias for the dashboard variable. This text will appear as the label for the dropdown field on the dashboard.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Replace<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable will only apply to charts that have a filter for the property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Restricted<wbr>Suggestions</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable may only be set to the values listed in `values_suggested` and only these values will appear in autosuggestion menus. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a value is required for this variable (and therefore whether it will be possible to view this dashboard without this filter applied). `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Values<wbr>Suggesteds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of strings of suggested values for this variable; these suggestions will receive priority when values are autosuggested for this variable.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>alias</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An alias for the dashboard variable. This text will appear as the label for the dropdown field on the dashboard.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>replace<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable will only apply to charts that have a filter for the property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>restricted<wbr>Suggestions</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable may only be set to the values listed in `values_suggested` and only these values will appear in autosuggestion menus. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines whether a value is required for this variable (and therefore whether it will be possible to view this dashboard without this filter applied). `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>values<wbr>Suggesteds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of strings of suggested values for this variable; these suggestions will receive priority when values are autosuggested for this variable.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>alias</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An alias for the dashboard variable. This text will appear as the label for the dropdown field on the dashboard.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>property</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a dimension to filter against.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>apply<wbr>If<wbr>Exist</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, this variable will also match data that doesn't have this property at all.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Variable description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>replace<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable will only apply to charts that have a filter for the property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>restricted<wbr>Suggestions</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If `true`, this variable may only be set to the values listed in `values_suggested` and only these values will appear in autosuggestion menus. `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether a value is required for this variable (and therefore whether it will be possible to view this dashboard without this filter applied). `false` by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of values to be used with the `property`, they will be combined via `OR`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>values<wbr>Suggesteds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of strings of suggested values for this variable; these suggestions will receive priority when values are autosuggested for this variable.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-signalfx">https://github.com/pulumi/pulumi-signalfx</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

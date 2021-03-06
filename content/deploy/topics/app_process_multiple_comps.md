# Install Multiple Components {#app_processs_multiple_comps .reference}

Install multiple components that are based on component tags or resource tags.

**Tip:** 

Applications, components, and generic processes share some process steps. This step applies only to application processes, including application processes that are associated with application templates.

It is up to you to select an appropriate component process to run. In most cases, select a component process of the Deployment type. If you select a different type of component process, you might get results that you do not expect. The server runs whatever component process you select, even if that process does not install the component. For example, if you select a component process of the Uninstall type, the Install Component step runs that component process as usual. Then, the component process uninstalls the component and removes the component from the inventory.

|Field|Description|
|-----|-----------|
|**Name**|A name for the step. Other process steps can refer to this step by this name.|
|**Component Tag**|A user-defined component tag that is used to select components. Only components with the specified tag are modified by this step.|
|**Component Process**|A process for the components that contain the selected tag. Only components that contain the process will run. Only one process can be selected per step.|
|**Limit to Resource Tag**|The user-defined resource tag that determines which resource runs the process. Only a resource with this tag, or a resource that has a parent with this tag, runs the process. See [Adding tags to objects](addingtags_tsk.md#).|
|**Use Versions Without Status**|Restricts the components that can be used by the step. Components with the selected status are ignored. Available statuses: Active means ignore components that are currently deployed.|
|**Maximum number of concurrent components**|The maximum number of components to deploy at one time. For example, if you specify 5, this step deploys five components at a time to all agents to which the components are mapped. To run this step on all components at the same time, specify `-1`. To limit the number of components to access at once, as in rolling deployments, specify an integer.The server attempts to resolve the value to an integer. If the value does not resolve to an integer, then the `-1` value is used by default. You can use a property in this field, as long as the property resolves to an integer.

**Note:** The maximum number of component processes that can run concurrently is limited by the hardware that hosts the agent.

|
|**Maximum number of concurrent processes**|The maximum number of concurrent processes to run, per component. This setting limits the number of processes that run simultaneously to deploy each component. For example, if you set the maximum number of concurrent processes to 2, only two instances of a component are installed at a time, even if many instances of the component are mapped to agents. To run an unlimited number of concurrent processes, specify `-1`. To limit the number of processes to run at once, as in rolling deployments, specify an integer.The server attempts to resolve the value to an integer. If the value does not resolve to an integer, then the `-1` value is used by default. You can use a property in this field, as long as the property resolves to an integer.

**Note:** The maximum number of component processes that can run concurrently is limited by the hardware that hosts the agent.

|
|**Fail Fast**|If this check box is selected, the step does not start more processes after one process fails.|
|**Precondition**|A JavaScript 1.7 script that defines a condition that must exist before the step can run. The condition must resolve to `true` or `false`. In the script, do not use the `${p:component.myProperty}` notation. For example, to check the value of a component property in a component process, use `properties.get("myProperty") == "myValue"`. See [Property contexts](ud_properties_context.md#) for information about property access.|

**Parent topic:** [Process steps: Reference](../topics/app_processSteps.md)


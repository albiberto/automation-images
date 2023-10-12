### {{issue.summary}}
<br/>

Enjoy **{{issue.reporter.displayName}}**, **{{issue.assignee.displayName}}** has completed the issue and moved it to **done** state.

### Issue Detail:
- **Key:** [{{key}}]({{url}})
- **Summary:** {{issue.summary}}
- **Type:** {{issue.issueType.name}}
- **Priority:** {{issue.priority.name}}
- **Status:** {{status.name}}
- **Reporter:** {{reporter.displayName}}
- **Assignee:** {{assignee.displayName}}
- **Start Date:** {{issue.Start Date.fullDate}}
- **Due Date:** {{issue.Due Date.fullDate}}
- **Original Estimate:** {{#if(issue.Original Estimate.lte(0))}}No Value Provided{{/}}{{#if(issue.Original Estimate.gt(0))}}{{#=}}FLOOR({{Original Estimate}} / 28800){{/}}d {{#=}}FLOOR(({{Original Estimate}} % 28800) / 3600){{/}}h {{#=}}FLOOR((({{Original Estimate}} % 28800) % 3600) / 60){{/}}m{{/}}
- **Time Spent:** {{#if(issue.TimeSpent.lte(0))}}No Value Provided{{/}}{{#if(issue.TimeSpent.gt(0))}}{{#=}}FLOOR({{TimeSpent}} / 28800){{/}}d {{#=}}FLOOR(({{TimeSpent}} % 28800) / 3600){{/}}h {{#=}}FLOOR((({{TimeSpent}} % 28800) % 3600) / 60){{/}}m{{/}}
- **Remaining Estimate:** {{#if(issue.Remaining Estimate.lte(0))}}No Value Provided{{/}}{{#if(issue.Remaining Estimate.gt(0))}}{{#=}}FLOOR({{Remaining Estimate}} / 28800){{/}}d {{#=}}FLOOR(({{Remaining Estimate}} % 28800) / 3600){{/}}h {{#=}}FLOOR((({{Remaining Estimate}} % 28800) % 3600) / 60){{/}}m{{/}}

{{#if(exists(issue.parent.key))}}
### Parent Detail:
- **Summary:** {{parent.summary}}
- **Key:** [{{issue.parent.key}}]({{issue.parent.url}})
- **Type:** {{issue.parent.issueType.name}}
- **Priority:** {{issue.parent.priority.name}}
- **Status:** {{issue.parent.status.name}}
- **Reporter:** {{parent.reporter.displayName}}
- **Assignee:** {{parent.assignee.displayName}}
{{/}}
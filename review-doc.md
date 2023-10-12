### {{issue.summary}}
<br/>

**{{issue.assignee.displayName}}**, review requests for issues related to the **documentation** component don't necessarily have to undergo a formal review, but we encourage you to ask any team member to take a look at the documentation and provide suggestions. Additionally, you are free to move the request to **done** state if you believe it's ready.

The documentation process is an ongoing journey, where the contribution of each team member is crucial to take it to exceptional levels. Every contribution, whether it's an idea, a review, or a suggestion, is valuable and will help enhance the quality of our documentation over time.

### Issue Detail:
- **Key:** [{{key}}]({{url}})
- **Type:** {{issue.issueType.name}}
- **Priority:** {{issue.priority.name}}
- **Status:** {{status.name}}
- **Reporter:** {{reporter.displayName}}
- **Assignee:** {{assignee.displayName}}
- **Start Date:** {{issue.Start Date.format("dd/MM/yyyy")}}
- **Due Date:** {{issue.Due Date.format("dd/MM/yyyy")}}
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
### {{issue.summary}}
<br/>

**{{issue.reporter.displayName}}** has moved **[{{key}}]({{url}})** in **Refined** state.

**{{issue.assignee.displayName}}**, please finalize this issue and move it to the **ToDo** state.

### Issue Detail:
- **Key:** [{{key}}]({{url}})
- **Type:** {{issue.issueType.name}}
- **Priority:** {{issue.priority.name}}
- **Status:** {{status.name}}
- **Reporter:** {{reporter.displayName}}
- **Assignee:** {{assignee.displayName}}

{{#if(exists(issue.parent.key))}}
### Parent Detail:
- **Summary:** {{issue.parent.summary}}
- **Key:** [{{issue.parent.key}}]({{issue.parent.url}})
- **Type:** {{issue.parent.issueType.name}}
- **Priority:** {{issue.parent.priority.name}}
- **Status:** {{issue.parent.status.name}}
- **Reporter:** {{parent.reporter.displayName}}
- **Assignee:** {{parent.assignee.displayName}}
{{/}}
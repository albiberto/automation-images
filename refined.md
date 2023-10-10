**{{issue.reporter.displayName}}** has moved **[{{key}}]({{url}})** in **Refined** state.

**{{issue.assignee.displayName}}**, please finalize this issue and move it to the **ToDo** state.

### Issue Detail:
- **Issue:** [{{key}}]({{url}})
- **Summary:** {{issue.summary}}
- **Type:** {{issue.issueType.name}}
- **Priority:** {{issue.priority.name}}
- **Status:** {{status.name}}
- **Reporter:** {{reporter.displayName}}
- **Assignee:** {{assignee.displayName}}

{{#if(exists(issue.parent.key))}}
### Parent Detail:
- **Parent:** [{{issue.parent.key}}]({{issue.parent.url}})
- **Summary:** {{parent.summary}}
- **Type:** {{issue.parent.issueType.name}}
- **Priority:** {{issue.parent.priority.name}}
- **Status:** {{issue.parent.status.name}}
- **Reporter:** {{parent.reporter.displayName}}
- **Assignee:** {{parent.assignee.displayName}}
{{/}}
# Learning Sessions

This directory stores your codebase learning sessions and findings. Each session is automatically saved when you use the codebase learning plugin commands.

## Directory Structure

Sessions are organized by type and timestamp:

```
.learning-sessions/
├── architecture-[timestamp].md    # Architecture analysis sessions
├── flow-[feature]-[timestamp].md  # Code flow tracing sessions
├── patterns-[timestamp].md        # Pattern detection sessions
├── concepts-[name]-[timestamp].md # Domain concept exploration sessions
└── index.md                       # Auto-generated index of all sessions
```

## Session File Format

Each session file contains:
- **Date & Time**: When the learning session occurred
- **Focus Area**: What was studied (architecture, flow, patterns, or concepts)
- **Scope**: What part of the codebase was analyzed
- **Key Findings**: Main insights and discoveries
- **Code References**: Links to relevant files and line numbers
- **Diagrams**: Visual representations (if applicable)
- **Next Steps**: Suggested areas for further exploration
- **Tags**: Keywords for easy searching

## Using Saved Sessions

### Quick Reference
Browse saved sessions to quickly recall what you've learned about different parts of the codebase.

### Build Knowledge Base
Over time, your sessions form a comprehensive knowledge base about the codebase.

### Share with Team
Share session files with team members to help them learn the codebase faster.

### Track Progress
Use the index file to see what areas you've explored and what's still unknown.

### Connect Learning
Sessions cross-reference each other, showing how different aspects of the codebase relate.

## Index File

The `index.md` file is automatically updated with each new session and provides:
- Chronological list of all sessions
- Sessions grouped by type
- Quick navigation to specific topics
- Coverage map showing explored areas

## Tips

1. **Regular Sessions**: Make learning sessions a regular practice
2. **Take Notes**: Add your own notes and questions to session files
3. **Connect Sessions**: Link related sessions together
4. **Review Periodically**: Revisit old sessions to reinforce learning
5. **Share Insights**: Share valuable sessions with your team

## Search Sessions

Use grep to search across all your learning sessions:

```bash
# Find sessions about authentication
grep -r "authentication" .learning-sessions/

# Find all architecture sessions
ls .learning-sessions/architecture-*.md

# Search for specific patterns
grep -r "Factory pattern" .learning-sessions/
```

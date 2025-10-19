# Codebase Learning Plugin for Claude Code

A comprehensive Claude Code plugin designed to help developers learn and understand codebases through specialized AI agents and interactive commands. Whether you're onboarding to a new project, exploring unfamiliar code, or deepening your architectural understanding, this plugin provides structured learning paths and detailed insights.

## Table of Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Commands Reference](#commands-reference)
- [Usage Examples](#usage-examples)
- [Output Formats](#output-formats)
- [Best Practices](#best-practices)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [License](#license)

## Features

### 🏗️ Architecture Analysis
- Analyze system architecture and design decisions
- Understand layer separation and module organization
- Visualize component relationships and dependencies
- Learn about architectural patterns in use

### 🔍 Code Flow Tracing
- Trace feature implementations end-to-end
- Understand execution paths and data flow
- Map function call sequences
- Identify key decision points and logic

### 🎨 Pattern Detection
- Identify design patterns (Gang of Four)
- Discover architectural patterns
- Analyze coding conventions and best practices
- Learn from pattern implementations

### 💡 Domain Concept Exploration
- Understand business logic and domain rules
- Learn domain-specific terminology
- Map concepts to code implementations
- Explore entity relationships and workflows

### 🎯 Interactive Output Formats
Choose your preferred learning style:
- **Interactive Documentation**: Detailed markdown with diagrams and cross-references
- **Guided Exploration**: Step-by-step walkthroughs
- **Visual Diagrams**: Mermaid charts showing structure and relationships
- **Structured Notes**: Organized summaries for quick reference

## Quick Start

### 1. Install the Plugin

**Option A: Install from Marketplace (Recommended)**
```bash
# Add the marketplace
/plugin marketplace add Jsnnmsc/claude-code-learning-marketplace

# Install the plugin
/plugin install codebase-learning@Jsnn-marketplace
```

**Option B: Install from GitHub**
```bash
# Clone the repository
git clone https://github.com/Jsnnmsc/claude-code-learning-marketplace.git

# Install via Claude Code
cd claude-code-learning-marketplace
claude-code plugin install .
```

Verify installation:
```bash
# In Claude Code
/plugin list
# Should show "codebase-learning"
```

### 2. First Learning Session

Start with the interactive learning command:

```bash
/learn
```

Claude will ask you:
1. **What to learn?** Choose "Architecture & Design Patterns"
2. **Scope?** Choose "Entire codebase overview"
3. **Output format?** Choose "Interactive Documentation"

The Architecture Analyzer agent will analyze your codebase and provide a comprehensive overview!

### 3. View Results

The analysis will be automatically saved to a markdown file in `.codebase-analysis/` directory. You can open this file in your editor for better viewing with:
- Formatted markdown
- Rendered diagrams
- Clickable file references
- Easy navigation

### 4. Explore Different Aspects

```bash
# Trace how a feature works
/learn-flow authentication

# Discover design patterns
/learn-patterns

# Understand domain concepts
/learn-concepts order-processing
```

## Installation

### Prerequisites

Before installing, ensure you have:

1. **Claude Code** installed and configured
   - Download from: https://claude.com/claude-code
   - Verify installation: `claude-code --version`

2. **Git** (for cloning the repository)
   - Install: https://git-scm.com/downloads
   - Verify: `git --version`

### Install from GitHub

1. **Clone the repository**
   ```bash
   git clone https://github.com/Jsnnmsc/claude-code-learning-marketplace.git
   cd claude-code-learning-marketplace
   ```

2. **Install the plugin**
   ```bash
   # Method 1: Using Claude Code CLI
   claude-code plugin install .

   # Method 2: Copy to plugins directory
   # Linux/macOS:
   mkdir -p ~/.claude-code/plugins
   cp -r . ~/.claude-code/plugins/codebase-learning

   # Windows:
   # Copy to %USERPROFILE%\.claude-code\plugins\codebase-learning
   ```

3. **Verify installation**
   ```bash
   # In Claude Code
   /plugin list
   # Should show "codebase-learning" in the list
   ```

4. **Enable the plugin** (if not auto-enabled)
   ```bash
   /plugin enable codebase-learning
   ```

### Install from Marketplace

Install directly via Claude Code marketplace:

```bash
# Add the marketplace
/plugin marketplace add Jsnnmsc/claude-code-learning-marketplace

# Install the plugin
/plugin install codebase-learning@Jsnn-marketplace
```

## Commands Reference

### `/learn`
**Description**: Interactive entry point for codebase learning

**Usage**: `/learn`

**What it does**:
- Asks what aspect of the codebase you want to explore
- Guides you to the appropriate specialized command
- Provides personalized learning path recommendations

---

### `/learn-architecture`
**Description**: Analyze system architecture and design decisions

**Usage**: `/learn-architecture`

**Best for**:
- Understanding overall system structure
- Learning about layer organization
- Discovering architectural patterns
- Mapping component dependencies

**Example Output**:
- High-level architecture diagrams
- Layer separation analysis
- Component dependency maps
- Design decision explanations

---

### `/learn-flow [feature-name]`
**Description**: Trace code execution paths for specific features

**Usage**: `/learn-flow <feature-name>`

**Examples**:
- `/learn-flow user-login`
- `/learn-flow data-processing`
- `/learn-flow api-request`

**Best for**:
- Understanding how features work
- Debugging complex logic
- Learning control flow
- Tracing data transformations

**Example Output**:
- Entry point identification
- Step-by-step execution trace
- Data flow diagrams
- Sequence diagrams

---

### `/learn-patterns`
**Description**: Identify design patterns and coding conventions

**Usage**: `/learn-patterns`

**Best for**:
- Discovering patterns in use
- Learning best practices
- Understanding code organization
- Identifying refactoring opportunities

**Example Output**:
- Design pattern catalog
- Architectural pattern analysis
- Coding convention documentation
- Pattern consistency report

---

### `/learn-concepts [concept-name]`
**Description**: Explore domain concepts and business logic

**Usage**: `/learn-concepts <concept-name>`

**Examples**:
- `/learn-concepts order-fulfillment`
- `/learn-concepts user-permissions`
- `/learn-concepts pricing-rules`

**Best for**:
- Understanding business logic
- Learning domain terminology
- Mapping concepts to code
- Exploring entity relationships

**Example Output**:
- Business concept explanations
- Domain model diagrams
- Business rules documentation
- Code-to-concept mappings

## Usage Examples

### Example 1: Learning a New Codebase

You've just joined a project and want to understand its architecture:

```bash
/learn-architecture
```

The plugin will:
1. Ask for your preferred output format
2. Ask what scope to analyze (full system, specific module, etc.)
3. Launch the Architecture Analyzer agent
4. Save the analysis to `.codebase-analysis/architecture-[timestamp].md`
5. Display the results and provide the file path
6. Suggest related areas to explore

You can then open the markdown file in your editor for better viewing.

### Example 2: Understanding a Feature

You need to fix a bug in the authentication system:

```bash
/learn-flow authentication
```

The plugin will:
1. Ask for output format preference
2. Find the authentication entry point
3. Trace the complete execution path
4. Save the flow analysis to `.codebase-analysis/flow-authentication-[timestamp].md`
5. Display the results and provide the file path

Open the file in your editor to see the complete flow trace with diagrams.

### Example 3: Learning Domain Concepts

You're working with a complex business domain:

```bash
/learn-concepts payment-processing
```

The plugin will:
1. Ask for exploration depth (overview/implementation/complete)
2. Ask for output format
3. Analyze the domain concept
4. Save the explanation to `.codebase-analysis/concepts-payment-processing-[timestamp].md`
5. Display the results and provide the file path

View the file in your editor to understand the business logic and code mapping.

### Example 4: Pattern Discovery

You want to understand how the codebase is structured:

```bash
/learn-patterns
```

The plugin will:
1. Ask what patterns to look for (design/architectural/conventions/all)
2. Ask for analysis scope
3. Scan and identify patterns
4. Save the pattern catalog to `.codebase-analysis/patterns-[timestamp].md`
5. Display the results and provide the file path

Open the file to browse the complete pattern catalog with examples.

## Analysis Results Storage

All analysis results are automatically saved to the `.codebase-analysis/` directory:

```
.codebase-analysis/
├── README.md                              # Directory documentation
├── architecture-2025-01-19-14-30.md      # Architecture analyses
├── flow-authentication-2025-01-19-15-00.md  # Flow traces
├── patterns-2025-01-19-16-00.md          # Pattern detections
└── concepts-payment-2025-01-20-10-00.md  # Concept explorations
```

### Benefits of Saved Files

- **Better Viewing**: Open in your editor for:
  - Syntax highlighting
  - Rendered Mermaid diagrams
  - Clickable file references
  - Proper markdown formatting

- **Easy Navigation**: Use your editor's:
  - Outline view for quick navigation
  - Search functionality
  - Split view for comparing analyses

- **Version Control**: Choose to:
  - Keep analyses private (default, in `.gitignore`)
  - Commit as team documentation
  - Share specific analyses with teammates

### Managing Analysis Files

**View all analyses**:
```bash
ls .codebase-analysis/
```

**Search across analyses**:
```bash
grep -r "authentication" .codebase-analysis/
```

**Open in editor**:
```bash
# Or simply click the file path provided after analysis
code .codebase-analysis/architecture-*.md
```

## Output Formats

### Interactive Documentation
- Comprehensive markdown documents
- Hierarchical structure for easy navigation
- Mermaid diagrams and visualizations
- Code snippets with file references
- Cross-references between sections
- "Deep dive" sections for complex topics

**Best for**: Thorough understanding, reference documentation, sharing with team

### Guided Exploration
- Step-by-step walkthroughs
- Progressive disclosure of complexity
- "Follow along" navigation instructions
- Questions to ponder at each step
- Exercises to reinforce learning
- Multiple exploration paths

**Best for**: Hands-on learning, onboarding, teaching others

### Visual Diagrams
- Architecture diagrams (C4 model style)
- Sequence diagrams for flows
- Class and entity relationship diagrams
- Flowcharts for logic paths
- All diagrams in Mermaid format

**Best for**: Visual learners, presentations, architectural documentation

### Structured Notes
- Concise bullet-point summaries
- Quick reference format
- Key findings highlighted
- File location index
- Pattern catalogs
- Decision logs

**Best for**: Quick lookups, cheat sheets, summaries

## Best Practices

### For Learning New Codebases
1. Start with `/learn-architecture` to get the big picture
2. Use `/learn-patterns` to understand conventions
3. Trace important features with `/learn-flow`
4. Dive into domain concepts with `/learn-concepts`

### For Debugging
1. Use `/learn-flow` to trace the problematic feature
2. Use `/learn-concepts` to understand related domain logic
3. Use `/learn-patterns` to identify if patterns are misapplied

### For Code Review
1. Use `/learn-patterns` to check consistency
2. Use `/learn-architecture` to verify architectural compliance
3. Use `/learn-concepts` to validate business logic

### For Documentation
1. Copy analysis results to create team documentation
2. Use visual diagram output for architecture docs
3. Create concept glossaries with `/learn-concepts`
4. Build pattern catalogs with `/learn-patterns`

### Common Workflows

#### Onboarding to New Codebase
```bash
# 1. Understand architecture
/learn-architecture

# 2. Discover patterns
/learn-patterns

# 3. Trace key features
/learn-flow user-login
/learn-flow data-processing

# 4. Learn domain concepts
/learn-concepts [main-business-concept]
```

#### Debugging a Bug
```bash
# 1. Trace the problematic feature
/learn-flow [buggy-feature]

# 2. Understand related domain logic
/learn-concepts [related-concept]

# 3. Check patterns for context
/learn-patterns
```

#### Code Review Preparation
```bash
# 1. Review architecture
/learn-architecture

# 2. Check pattern consistency
/learn-patterns

# 3. Validate domain logic
/learn-concepts [feature-domain]
```

## Troubleshooting

### Plugin not loading

**Problem**: Plugin doesn't appear in `/plugin list`

**Solutions**:
1. Check installation directory:
   ```bash
   ls ~/.claude-code/plugins/codebase-learning
   ```
   Should show `.claude-plugin/plugin.json` and other files

2. Verify plugin.json syntax:
   ```bash
   cat ~/.claude-code/plugins/codebase-learning/.claude-plugin/plugin.json
   ```
   Should be valid JSON

3. Reinstall the plugin:
   ```bash
   claude-code plugin install /path/to/plugin
   ```

### Commands not found

**Problem**: `/learn` commands don't work

**Solutions**:
1. Check plugin is enabled:
   ```bash
   /plugin list
   # Look for "codebase-learning" with "enabled" status
   ```

2. Enable if needed:
   ```bash
   /plugin enable codebase-learning
   ```

3. Restart Claude Code

### Agent not responding

**Problem**: Agents don't start or don't respond

**Solutions**:
- Check internet connection
- Verify Claude Code is properly authenticated
- Try the command again
- Check Claude Code has necessary permissions

## FAQ

**Q: Does this plugin modify my code?**

A: No, the plugin is read-only. It only analyzes and documents your code.

---

**Q: Will it work with any programming language?**

A: Yes! The agents are language-agnostic and work with any codebase.

---

**Q: How long does analysis take?**

A: Depends on codebase size. Small projects: 1-2 minutes. Large projects: 5-10 minutes.

---

**Q: Can I customize the agents?**

A: Yes! Agent prompts are in markdown files (`agents/*.md`) and can be edited to fit your needs.

---

**Q: Is my code sent to external servers?**

A: The plugin uses Claude Code's AI, which sends code snippets to Anthropic's servers for analysis. Review Anthropic's privacy policy for details.

---

**Q: Can I use this for proprietary codebases?**

A: Yes, but review your company's policies regarding AI code analysis tools.

---

**Q: How accurate is the analysis?**

A: Very accurate for understanding structure and patterns. For critical decisions, always verify findings.

---

**Q: What if I want different output than the predefined formats?**

A: You can edit the agent prompts in the `agents/` directory to customize the output format and content.

## Specialized Agents

The plugin uses four specialized AI agents, each designed for specific learning tasks:

### Architecture Analyzer
- Analyzes system architecture at multiple levels
- Identifies architectural patterns and styles
- Maps component dependencies
- Explains design decisions and trade-offs
- Creates architecture diagrams

### Code Flow Tracer
- Traces execution paths from entry to exit
- Maps data transformations
- Identifies decision points
- Explains control flow logic
- Creates sequence diagrams

### Pattern Detector
- Identifies Gang of Four design patterns
- Discovers architectural patterns
- Analyzes coding conventions
- Assesses pattern consistency
- Creates pattern catalogs

### Concept Explainer
- Explains business concepts
- Maps domain to code
- Documents business rules
- Shows entity relationships
- Creates domain models

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Credits

Created for the Claude Code community to make codebase learning more accessible and effective.

## Support

- **Issues**: [GitHub Issues](https://github.com/Jsnnmsc/claude-code-learning-marketplace/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Jsnnmsc/claude-code-learning-marketplace/discussions)

---

**Happy Learning! 📚**

Start your codebase learning journey with `/learn`

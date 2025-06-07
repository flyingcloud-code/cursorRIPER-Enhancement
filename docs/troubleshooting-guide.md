![CursorRIPER](../res/github-header.png)
# CursorRIPER Framework - Troubleshooting Guide

This guide helps you identify and resolve common issues that may arise when using the CursorRIPER Framework. Whether you're experiencing setup problems, workflow disruptions, or unexpected behavior, you'll find diagnostic steps and solutions here.

## Table of Contents

1. [Installation and Setup Issues](#installation-and-setup-issues)
2. [File Extension Issues](#file-extension-issues)
3. [State Management Problems](#state-management-problems)
4. [Memory Bank Issues](#memory-bank-issues)
5. [Workflow Disruptions](#workflow-disruptions)
6. [Cursor IDE Integration](#cursor-ide-integration)
7. [Customization Challenges](#customization-challenges)
8. [Recovery Procedures](#recovery-procedures)
9. [Performance Considerations](#performance-considerations)

## Installation and Setup Issues

### Framework Files Not Found

**Symptoms:**
- AI doesn't recognize CursorRIPER commands
- Error messages about missing framework files
- AI doesn't acknowledge the framework in responses

**Possible Causes:**
- Files not copied to the correct location
- Files have incorrect names or extensions
- Cursor not recognizing the framework files

**Solutions:**
1. Verify files exist in `.cursor/rules/` directory
2. Ensure all framework files have `.mdc` extension (not `.md`)
3. Check file permissions
4. Restart Cursor IDE to reload framework files

### Framework Not Initializing

**Symptoms:**
- `/start` command doesn't trigger START phase
- No acknowledgment of framework initialization

**Possible Causes:**
- Core files missing or corrupted
- File paths incorrect
- Conflicts with other Cursor rules

**Solutions:**
1. Verify core.mdc and state.mdc exist and are properly formatted
2. Check console for any error messages
3. Try manually setting state.mdc to `PROJECT_PHASE: "UNINITIATED"`
4. Reinstall framework files from source

## File Extension Issues

### GitHub Repository vs. Project Files

**Important Note:** In the GitHub repository, framework files use `.md` extension for proper rendering on GitHub. When implementing in your project, these files must be renamed to use the `.mdc` extension.

**Symptoms:**
- Framework not loading properly
- AI not recognizing framework commands
- No mode declarations in AI responses

**Solution:**
1. Download framework files from GitHub
2. Rename all framework rule files from `.md` to `.mdc`:
   ```bash
   # Linux/macOS
   cd .cursor/rules/
   for file in *.md; do mv "$file" "${file%.md}.mdc"; done
   
   # Windows PowerShell
   Get-ChildItem -Path ".cursor\rules" -Filter "*.md" | Rename-Item -NewName { $_.Name -replace '.md','.mdc' }
   ```
3. Leave files in the `memory-bank/` directory with `.md` extension
4. Restart Cursor IDE

### Files to Rename

These files must be renamed from `.md` to `.mdc`:
- `core.md` → `core.mdc`
- `state.md` → `state.mdc`
- `start-phase.md` → `start-phase.mdc`
- `riper-workflow.md` → `riper-workflow.mdc`
- `customization.md` → `customization.mdc`

## State Management Problems

### Incorrect Mode or Phase

**Symptoms:**
- AI using wrong mode declaration
- Commands not triggering mode changes
- Inconsistent behavior between sessions

**Possible Causes:**
- Corrupted state.mdc file
- Incomplete mode transition
- File save issues

**Solutions:**
1. Examine state.mdc file to check current values
2. Manually update state values to correct settings:
   ```
   PROJECT_PHASE: "DEVELOPMENT"
   RIPER_CURRENT_MODE: "RESEARCH"
   ```
3. Reset framework state:
   ```
   Please reset the framework state to DEVELOPMENT phase and RESEARCH mode.
   ```

### Re-initialization Issues

**Symptoms:**
- Unable to restart project
- "/start" command not recognized after previous initialization
- Error messages about re-initialization

**Possible Causes:**
- Framework protecting against accidental re-initialization
- Corrupted state file
- Missing confirmation

**Solutions:**
1. Use explicit re-initialization confirmation:
   ```
   /start
   CONFIRM RE-INITIALIZATION
   ```
2. If still failing, manually edit state.mdc:
   ```
   PROJECT_PHASE: "UNINITIATED"
   START_PHASE_STATUS: "NOT_STARTED"
   ```
3. If needed, delete and reinstall framework files

## Memory Bank Issues

### Missing or Corrupted Memory Files

**Symptoms:**
- AI lacks project context
- Error messages about missing memory files
- Incomplete or nonsensical responses

**Possible Causes:**
- Files deleted or moved
- Improper updates corrupting files
- Permission issues preventing saves

**Solutions:**
1. Check if files exist in memory-bank directory
2. Restore from backups if available:
   ```
   memory-bank/backups/[date]/
   ```
3. If no backups, ask AI to recreate basic memory files:
   ```
   Please recreate the missing memory bank files based on our current project state.
   ```

### Inconsistent Information

**Symptoms:**
- AI gives contradictory responses
- References to outdated or incorrect information
- Confusion about project requirements or status

**Possible Causes:**
- Memory files updated inconsistently
- Multiple team members making uncoordinated changes
- Manual edits with formatting errors

**Solutions:**
1. Review all memory files for consistency
2. Update timestamp and version in all files
3. Ask AI to reconcile inconsistencies:
   ```
   Please review all memory files and reconcile any inconsistencies in project information.
   ```
4. Consider full memory bank refresh for severe issues

## Workflow Disruptions

### Mode Constraints Not Being Followed

**Symptoms:**
- AI making suggestions in RESEARCH mode
- Implementing code in PLAN mode
- Not following approved plan in EXECUTE mode

**Possible Causes:**
- Mode not properly declared
- State file inconsistency
- AI context limitations

**Solutions:**
1. Explicitly reinforce mode constraints:
   ```
   You are in RESEARCH mode. Please only gather information and ask questions.
   ```
2. Restart chat session to refresh AI context
3. Verify state.mdc shows correct mode
4. Use Cursor's Custom Modes if available (see custom-modes-guide.md)

### Problems with PLAN Mode Checklist

**Symptoms:**
- No checklist generated
- Incomplete or vague checklist items
- Checklist not reflecting full implementation needs

**Possible Causes:**
- Insufficient information provided
- Complex requirements not fully articulated
- AI context limitations

**Solutions:**
1. Explicitly request a detailed checklist:
   ```
   Please generate a comprehensive, numbered implementation checklist with specific, actionable steps.
   ```
2. Provide more detailed requirements
3. Break complex features into smaller components
4. Adjust PLAN_QUESTION_COUNT in customization.mdc

### EXECUTE Mode Implementation Issues

**Symptoms:**
- AI deviating from approved plan
- Incomplete implementation
- Errors during implementation

**Possible Causes:**
- Plan not detailed enough
- Technical challenges not anticipated
- Ambiguities in plan steps

**Solutions:**
1. Return to PLAN mode if deviation needed:
   ```
   /plan
   We need to revise our plan to handle this unexpected issue.
   ```
2. Create more detailed implementation checklists
3. Update progress.md when issues are encountered
4. Break complex implementations into smaller steps

## Cursor IDE Integration

### MDC Files Not Recognized

**Symptoms:**
- Framework not loading
- Rules not appearing in Cursor settings
- No framework behavior observed

**Possible Causes:**
- Incorrect file location
- Incorrect file format
- Cursor IDE version incompatibility

**Solutions:**
1. Ensure files are in `.cursor/rules/` directory
2. Verify files have `.mdc` extension
3. Check Cursor documentation for current Rules format
4. Restart Cursor IDE
5. Update Cursor to latest version

### Command Recognition Failures

**Symptoms:**
- Commands like `/research` not triggering mode changes
- AI not responding to framework commands
- Inconsistent command recognition

**Possible Causes:**
- AI context limitations
- Command format issues
- Cursor IDE version differences

**Solutions:**
1. Try alternative command format:
   - If `/research` fails, try `ENTER RESEARCH MODE`
2. Explicitly define command in your message:
   ```
   I want to switch to RESEARCH mode. Please transition and begin operating in that mode.
   ```
3. Restart chat session to refresh AI context
4. Check custom commands in customization.mdc

## Customization Challenges

### Customization Not Applied

**Symptoms:**
- Default behavior persists despite customization
- No acknowledgment of custom settings
- Incorrect verbosity or behavior

**Possible Causes:**
- customization.mdc missing or not loaded
- Syntax errors in customization file
- Custom settings overridden elsewhere

**Solutions:**
1. Verify customization.mdc exists in `.cursor/rules/`
2. Check for syntax errors or formatting issues
3. Restart Cursor IDE to reload settings
4. Try explicit settings request:
   ```
   Please acknowledge and apply my custom settings from customization.mdc.
   ```

### Formatting Errors

**Symptoms:**
- Error messages related to customization
- Framework loading with default settings
- Unexpected behavior

**Possible Causes:**
- Invalid syntax in customization.mdc
- Incorrect value types
- Missing required fields

**Solutions:**
1. Check customization.mdc against the template
2. Verify all values use correct types and formats
3. Remove problematic settings to isolate issues
4. Restore from default customization.mdc template

## Recovery Procedures

### Restoring from Backups

If you have automatic backups enabled (see `BACKUP_FREQUENCY` in customization.mdc), you can restore from them:

1. Locate backup directory (typically `memory-bank/backups/[date]/`)
2. Copy desired backup files to main memory-bank directory
3. Update state.mdc if needed
4. Restart Cursor IDE

### Manual State Reset

If framework state becomes corrupted:

1. Edit state.mdc manually:
   ```
   PROJECT_PHASE: "DEVELOPMENT"
   RIPER_CURRENT_MODE: "RESEARCH"
   START_PHASE_STATUS: "COMPLETED"
   START_PHASE_STEP: 6
   LAST_UPDATE: "[current date in ISO format]"
   ```
2. Restart Cursor IDE
3. Inform AI of correct state:
   ```
   The framework state has been manually reset to DEVELOPMENT phase and RESEARCH mode.
   ```

### Rebuilding Memory Bank

For severe corruption or missing memory files:

1. Create a backup of any existing memory files
2. Delete corrupted memory files
3. Ask AI to rebuild essential memory:
   ```
   Please rebuild our memory bank files based on the current project state and what you know about our work so far.
   ```
4. Review and supplement generated files with missing information

### Emergency Rollback

If destructive code changes occurred:

1. Use version control to revert changes:
   ```bash
   git checkout -- path/to/changed/files
   ```
2. If no version control, check for automatic backups in your editor
3. Update memory files to reflect rollback:
   ```
   Please update the memory bank to reflect that we've rolled back changes to [feature/component].
   ```

## Performance Considerations

### Slow AI Responses

**Symptoms:**
- Long delays in AI responses
- Incomplete or truncated responses
- AI appearing to lose context

**Possible Causes:**
- Very large memory files
- Complex project structure
- Resource limitations

**Solutions:**
1. Reduce size of memory files by focusing on essential information
2. Archive older, less relevant content
3. Split large memory files into component parts
4. Restart Cursor IDE to clear memory

### Memory Consumption Issues

**Symptoms:**
- Cursor IDE running slowly
- High CPU or memory usage
- Frequent freezing or crashing

**Possible Causes:**
- Large codebase with extensive indexing
- Many large memory files
- Cursor IDE resource limitations

**Solutions:**
1. Use .cursorignore file to exclude non-essential directories
2. Optimize memory files by removing redundant information
3. Consider running Cursor with additional resources
4. Restart Cursor IDE periodically to clear memory

---

## Contacting Support

If you continue to experience issues after trying these troubleshooting steps:

1. Check the official CursorRIPER repository for updates and known issues
2. Review Cursor IDE documentation for any relevant information
3. Consider posting an issue on the CursorRIPER GitHub repository

---

*The CursorRIPER Framework prevents coding disasters while maintaining perfect continuity across sessions.*

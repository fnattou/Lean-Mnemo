Save session insights to `memory/` following `memory-format.aicontext`.

## Steps

1. **Analyze**: Read `$ARGUMENTS`, extract 3-5 key insights
2. **Determine category and topic**: Choose from existing categories (`decisions/`, `tasks/`, `bugs/`, etc.) or create a new one
3. **Write**:
   - If `memory/{category}/{topic}.aicontext` exists → read, merge, update date
   - If not → create new file
   - Format: YAML + DSL as defined in `memory-format.aicontext`
4. **Update indices**: Update `memory/{category}/index.aicontext`; if new category, also update `memory/index.aicontext`
5. **Suggest dict entries**: If any 3+ token term appears 3+ times, propose adding to `dict.aicontext`

## $ARGUMENTS

Context to save (conversation, decisions, tasks, etc.): $ARGUMENTS
# ui

## 1.10.0-next.8

### Patch Changes

- 6de24ce: - fix rerender issues by moving suggestions to the messages context
  - @copilotkit/runtime-client-gql@1.10.0-next.8
  - @copilotkit/shared@1.10.0-next.8

## 1.10.0-next.7

### Patch Changes

- @copilotkit/runtime-client-gql@1.10.0-next.7
- @copilotkit/shared@1.10.0-next.7

## 1.10.0-next.6

### Patch Changes

- @copilotkit/runtime-client-gql@1.10.0-next.6
- @copilotkit/shared@1.10.0-next.6

## 1.10.0-next.5

### Patch Changes

- Updated dependencies [a8c0263]
  - @copilotkit/shared@1.10.0-next.5
  - @copilotkit/runtime-client-gql@1.10.0-next.5

## 1.10.0-next.4

### Patch Changes

- 967d0ab: - refactor(chat): separate useCopilotChat into internal implementation and public API
  - @copilotkit/runtime-client-gql@1.10.0-next.4
  - @copilotkit/shared@1.10.0-next.4

## 1.10.0-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.10.0-next.3
- @copilotkit/shared@1.10.0-next.3

## 1.10.0-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.10.0-next.2
- @copilotkit/shared@1.10.0-next.2

## 1.10.0-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.10.0-next.1
- @copilotkit/shared@1.10.0-next.1

## 1.10.0-next.0

### Minor Changes

- 8674da1: - refactor(headless): completely overhaul headless ui to better support agentic features

  Headless UI has been in a bad state for a bit now. When we added support for different
  agentic runtimes we acquired tech-debt that, with this PR, is being alleviated.

  As such, the following features have been updated to be completely functional with Headless UI.

  - Generative UI
  - Suggestions
  - Agentic Generative UI
  - Interrupts

  In addition, a variety of QOL changes have been made.

  - New AG-UI based message types
  - Inline code rendering is fixed

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

### Patch Changes

- Updated dependencies [8674da1]
  - @copilotkit/shared@1.10.0-next.0
  - @copilotkit/runtime-client-gql@1.10.0-next.0

## 1.9.3

### Patch Changes

- f83bda0: Fix: remote actions should never be executed to avoid duplicate result messages
- Updated dependencies [1bda332]
  - @copilotkit/shared@1.9.3
  - @copilotkit/runtime-client-gql@1.9.3

## 1.9.3-next.4

### Patch Changes

- f83bda0: Fix: remote actions should never be executed to avoid duplicate result messages
  - @copilotkit/runtime-client-gql@1.9.3-next.4
  - @copilotkit/shared@1.9.3-next.4

## 1.9.3-next.3

### Patch Changes

- Updated dependencies [1bda332]
  - @copilotkit/shared@1.9.3-next.3
  - @copilotkit/runtime-client-gql@1.9.3-next.3

## 1.9.3-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.3-next.2
- @copilotkit/shared@1.9.3-next.2

## 1.9.3-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.3-next.1
- @copilotkit/shared@1.9.3-next.1

## 1.9.3-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.3-next.0
- @copilotkit/shared@1.9.3-next.0

## 1.9.2

### Patch Changes

- cbeccb5: - fix: refrain repeated api calls by memoizing state
- 3f8c575: - fix: use time travel for regeneration of messages
  - fix: use a better cutoff for regeneration request
- fac89c2: - refactor: rename onTrace to onError throughout codebase

  - Rename CopilotTraceEvent to CopilotErrorEvent and CopilotTraceHandler to CopilotErrorHandler

- e1de032: - fix: synchronously execute renderAndWaitForResponse

  Previously, it was impossible to execute multiple human-in-the-loop (renderAndWaitForResponse)
  calls in a row. Ultimately this was due to an issue with how CopilotKit was rendering the updates
  when multiple renderAndWaitForResponse actions appeared on screen due to a reference based approach.

  With this change, actions will be executed in a synchronous way appearing almost queue like. This
  works with any combination of action given much more freedom when asking for user input.

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

- 92e8d1c: - fix infinite loop
- 9169ad7: - feat: add onTrace handler for runtime and UI error/event tracking
- c75a04f: - Fix dynamic runtime configuration updates in useCoAgent
  - In use-chat.ts, agent state updates from AgentStateMessage now preserve existing config property
- c75a04f: - Fix dynamic runtime configuration updates in useCoAgent
- fe9009c: - feat(langgraph): new thread metadata
- 1d1c51d: - feat: surface all errors in structured format
- 10345a5: - feat: structured error visibility system for streaming errors
- 9169ad7: - feat: add onTrace handler for comprehensive debugging and observability - Add CopilotTraceEvent interfaces with rich debugging context, implement runtime-side tracing with publicApiKey gating, add UI-side error tracing, include comprehensive test coverage, and fix tsup build config to exclude test files
  - fix: extract publicApiKey for all requests + trace GraphQL errors
- 35537f1: - fix: memoize nested components to not rerender when content changes
- Updated dependencies [fac89c2]
- Updated dependencies [9169ad7]
- Updated dependencies [1d1c51d]
- Updated dependencies [10345a5]
- Updated dependencies [9169ad7]
  - @copilotkit/shared@1.9.2
  - @copilotkit/runtime-client-gql@1.9.2

## 1.9.2-next.26

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.26
- @copilotkit/shared@1.9.2-next.26

## 1.9.2-next.25

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.25
- @copilotkit/shared@1.9.2-next.25

## 1.9.2-next.24

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.24
- @copilotkit/shared@1.9.2-next.24

## 1.9.2-next.23

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.23
- @copilotkit/shared@1.9.2-next.23

## 1.9.2-next.22

### Patch Changes

- c75a04f: - Fix dynamic runtime configuration updates in useCoAgent
  - In use-chat.ts, agent state updates from AgentStateMessage now preserve existing config property
- c75a04f: - Fix dynamic runtime configuration updates in useCoAgent
  - @copilotkit/runtime-client-gql@1.9.2-next.22
  - @copilotkit/shared@1.9.2-next.22

## 1.9.2-next.21

### Patch Changes

- 92e8d1c: - fix infinite loop
  - @copilotkit/runtime-client-gql@1.9.2-next.21
  - @copilotkit/shared@1.9.2-next.21

## 1.9.2-next.20

### Patch Changes

- e1de032: - fix: synchronously execute renderAndWaitForResponse

  Previously, it was impossible to execute multiple human-in-the-loop (renderAndWaitForResponse)
  calls in a row. Ultimately this was due to an issue with how CopilotKit was rendering the updates
  when multiple renderAndWaitForResponse actions appeared on screen due to a reference based approach.

  With this change, actions will be executed in a synchronous way appearing almost queue like. This
  works with any combination of action given much more freedom when asking for user input.

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

  - @copilotkit/runtime-client-gql@1.9.2-next.20
  - @copilotkit/shared@1.9.2-next.20

## 1.9.2-next.19

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.19
- @copilotkit/shared@1.9.2-next.19

## 1.9.2-next.18

### Patch Changes

- fac89c2: - refactor: rename onTrace to onError throughout codebase

  - Rename CopilotTraceEvent to CopilotErrorEvent and CopilotTraceHandler to CopilotErrorHandler

- Updated dependencies [fac89c2]
  - @copilotkit/shared@1.9.2-next.18
  - @copilotkit/runtime-client-gql@1.9.2-next.18

## 1.9.2-next.17

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.17
- @copilotkit/shared@1.9.2-next.17

## 1.9.2-next.16

### Patch Changes

- fe9009c: - feat(langgraph): new thread metadata
  - @copilotkit/runtime-client-gql@1.9.2-next.16
  - @copilotkit/shared@1.9.2-next.16

## 1.9.2-next.15

### Patch Changes

- cbeccb5: - fix: refrain repeated api calls by memoizing state
  - @copilotkit/runtime-client-gql@1.9.2-next.15
  - @copilotkit/shared@1.9.2-next.15

## 1.9.2-next.14

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.14
- @copilotkit/shared@1.9.2-next.14

## 1.9.2-next.13

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.13
- @copilotkit/shared@1.9.2-next.13

## 1.9.2-next.12

### Patch Changes

- 3f8c575: - fix: use time travel for regeneration of messages
  - fix: use a better cutoff for regeneration request
  - @copilotkit/runtime-client-gql@1.9.2-next.12
  - @copilotkit/shared@1.9.2-next.12

## 1.9.2-next.11

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.11
- @copilotkit/shared@1.9.2-next.11

## 1.9.2-next.10

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.10
- @copilotkit/shared@1.9.2-next.10

## 1.9.2-next.9

### Patch Changes

- 1d1c51d: - feat: surface all errors in structured format
- Updated dependencies [1d1c51d]
  - @copilotkit/runtime-client-gql@1.9.2-next.9
  - @copilotkit/shared@1.9.2-next.9

## 1.9.2-next.8

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.8
- @copilotkit/shared@1.9.2-next.8

## 1.9.2-next.7

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.7
- @copilotkit/shared@1.9.2-next.7

## 1.9.2-next.6

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.6
- @copilotkit/shared@1.9.2-next.6

## 1.9.2-next.5

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.5
- @copilotkit/shared@1.9.2-next.5

## 1.9.2-next.4

### Patch Changes

- 9169ad7: - feat: add onTrace handler for runtime and UI error/event tracking
- 9169ad7: - feat: add onTrace handler for comprehensive debugging and observability - Add CopilotTraceEvent interfaces with rich debugging context, implement runtime-side tracing with publicApiKey gating, add UI-side error tracing, include comprehensive test coverage, and fix tsup build config to exclude test files
  - fix: extract publicApiKey for all requests + trace GraphQL errors
- Updated dependencies [9169ad7]
- Updated dependencies [9169ad7]
  - @copilotkit/shared@1.9.2-next.4
  - @copilotkit/runtime-client-gql@1.9.2-next.4

## 1.9.2-next.3

### Patch Changes

- 35537f1: - fix: memoize nested components to not rerender when content changes
  - @copilotkit/runtime-client-gql@1.9.2-next.3
  - @copilotkit/shared@1.9.2-next.3

## 1.9.2-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.2
- @copilotkit/shared@1.9.2-next.2

## 1.9.2-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.2-next.1
- @copilotkit/shared@1.9.2-next.1

## 1.9.2-next.0

### Patch Changes

- 10345a5: - feat: structured error visibility system for streaming errors
- Updated dependencies [10345a5]
  - @copilotkit/runtime-client-gql@1.9.2-next.0
  - @copilotkit/shared@1.9.2-next.0

## 1.9.1

### Patch Changes

- Updated dependencies [deaeca0]
  - @copilotkit/shared@1.9.1
  - @copilotkit/runtime-client-gql@1.9.1

## 1.9.1-next.0

### Patch Changes

- Updated dependencies [deaeca0]
  - @copilotkit/shared@1.9.1-next.0
  - @copilotkit/runtime-client-gql@1.9.1-next.0

## 1.9.0

### Patch Changes

- 54cae30: - fix(react-core): allow custom toolChoice in forwardedParameters to override default
  - fix: move react-dom to peerDependencies in @copilotkit/react-textarea
  - feat: add amazon bedrock adapter support
  - @copilotkit/runtime-client-gql@1.9.0
  - @copilotkit/shared@1.9.0

## 1.9.0-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.9.0-next.2
- @copilotkit/shared@1.9.0-next.2

## 1.8.15-next.1

### Patch Changes

- 54cae30: - fix(react-core): allow custom toolChoice in forwardedParameters to override default
  - fix: move react-dom to peerDependencies in @copilotkit/react-textarea
  - feat: add amazon bedrock adapter support
  - @copilotkit/runtime-client-gql@1.8.15-next.1
  - @copilotkit/shared@1.8.15-next.1

## 1.8.15-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.15-next.0
- @copilotkit/shared@1.8.15-next.0

## 1.8.14

### Patch Changes

- 9cf1fda: - fix append follow-up when actions disable followUp
  - Create stupid-nails-travel.md
  - fixup
- 9cf1fda: - fix append follow-up when actions disable followUp
- Updated dependencies [34a78d8]
  - @copilotkit/shared@1.8.14
  - @copilotkit/runtime-client-gql@1.8.14

## 1.8.14-next.5

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.14-next.5
- @copilotkit/shared@1.8.14-next.5

## 1.8.14-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.14-next.4
- @copilotkit/shared@1.8.14-next.4

## 1.8.14-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.14-next.3
- @copilotkit/shared@1.8.14-next.3

## 1.8.14-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.14-next.2
- @copilotkit/shared@1.8.14-next.2

## 1.8.14-next.1

### Patch Changes

- Updated dependencies [34a78d8]
  - @copilotkit/shared@1.8.14-next.1
  - @copilotkit/runtime-client-gql@1.8.14-next.1

## 1.8.14-next.0

### Patch Changes

- 9cf1fda: - fix append follow-up when actions disable followUp
  - Create stupid-nails-travel.md
  - fixup
- 9cf1fda: - fix append follow-up when actions disable followUp
  - @copilotkit/runtime-client-gql@1.8.14-next.0
  - @copilotkit/shared@1.8.14-next.0

## 1.8.13

### Patch Changes

- 7fcf5c4: - fix followUp check
  - @copilotkit/runtime-client-gql@1.8.13
  - @copilotkit/shared@1.8.13

## 1.8.13-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.13-next.3
- @copilotkit/shared@1.8.13-next.3

## 1.8.13-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.13-next.2
- @copilotkit/shared@1.8.13-next.2

## 1.8.13-next.1

### Patch Changes

- 7fcf5c4: - fix followUp check
  - @copilotkit/runtime-client-gql@1.8.13-next.1
  - @copilotkit/shared@1.8.13-next.1

## 1.8.13-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.13-next.0
- @copilotkit/shared@1.8.13-next.0

## 1.8.12

### Patch Changes

- 3e09584: - fix: stop passing config if not exists
- 33ba021: - partial revert of potentially breaking check
  - wip
  - @copilotkit/runtime-client-gql@1.8.12
  - @copilotkit/shared@1.8.12

## 1.8.12-next.6

### Patch Changes

- 3e09584: - fix: stop passing config if not exists
  - @copilotkit/runtime-client-gql@1.8.12-next.6
  - @copilotkit/shared@1.8.12-next.6

## 1.8.12-next.5

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.12-next.5
- @copilotkit/shared@1.8.12-next.5

## 1.8.12-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.12-next.4
- @copilotkit/shared@1.8.12-next.4

## 1.8.12-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.12-next.3
- @copilotkit/shared@1.8.12-next.3

## 1.8.12-next.2

### Patch Changes

- 33ba021: - partial revert of potentially breaking check
  - wip
  - @copilotkit/runtime-client-gql@1.8.12-next.2
  - @copilotkit/shared@1.8.12-next.2

## 1.8.12-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.12-next.1
- @copilotkit/shared@1.8.12-next.1

## 1.8.12-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.12-next.0
- @copilotkit/shared@1.8.12-next.0

## 1.8.11

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.11
- @copilotkit/shared@1.8.11

## 1.8.11-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.11-next.1
- @copilotkit/shared@1.8.11-next.1

## 1.8.11-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.11-next.0
- @copilotkit/shared@1.8.11-next.0

## 1.8.10

### Patch Changes

- 742efbb: - feat: enable setting langgraph config from ui
  - chore: document usage of new config
  - @copilotkit/runtime-client-gql@1.8.10
  - @copilotkit/shared@1.8.10

## 1.8.10-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.10-next.3
- @copilotkit/shared@1.8.10-next.3

## 1.8.10-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.10-next.2
- @copilotkit/shared@1.8.10-next.2

## 1.8.10-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.10-next.1
- @copilotkit/shared@1.8.10-next.1

## 1.8.10-next.0

### Patch Changes

- 742efbb: - feat: enable setting langgraph config from ui
  - chore: document usage of new config
  - @copilotkit/runtime-client-gql@1.8.10-next.0
  - @copilotkit/shared@1.8.10-next.0

## 1.8.9

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.9
- @copilotkit/shared@1.8.9

## 1.8.9-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.9-next.0
- @copilotkit/shared@1.8.9-next.0

## 1.8.8

### Patch Changes

- dfb67c3: - refactor: rename mcpEndpoints to mcpServers for naming consistency
  - doc changes
  - @copilotkit/runtime-client-gql@1.8.8
  - @copilotkit/shared@1.8.8

## 1.8.8-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.8-next.1
- @copilotkit/shared@1.8.8-next.1

## 1.8.8-next.0

### Patch Changes

- dfb67c3: - refactor: rename mcpEndpoints to mcpServers for naming consistency
  - doc changes
  - @copilotkit/runtime-client-gql@1.8.8-next.0
  - @copilotkit/shared@1.8.8-next.0

## 1.8.7

### Patch Changes

- Updated dependencies [8b8474f]
  - @copilotkit/runtime-client-gql@1.8.7
  - @copilotkit/shared@1.8.7

## 1.8.7-next.0

### Patch Changes

- Updated dependencies [8b8474f]
  - @copilotkit/runtime-client-gql@1.8.7-next.0
  - @copilotkit/shared@1.8.7-next.0

## 1.8.6

### Patch Changes

- 7a04bd1: - fix: fix how results are communicated back on interrupt
  - fix: do not allow followup for interrupt actions
  - chore: improve TS docs for interrupt
  - @copilotkit/runtime-client-gql@1.8.6
  - @copilotkit/shared@1.8.6

## 1.8.6-next.0

### Patch Changes

- 7a04bd1: - fix: fix how results are communicated back on interrupt
  - fix: do not allow followup for interrupt actions
  - chore: improve TS docs for interrupt
  - @copilotkit/runtime-client-gql@1.8.6-next.0
  - @copilotkit/shared@1.8.6-next.0

## 1.8.5

### Patch Changes

- c0d3261: - full AWP support

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

  - refactor: address linter issues with the new pages

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

  - Merge branch 'mme/acp' into mme/mastra
  - add sse example
  - Create small-turkeys-agree.md
  - upgrade AWP
  - Merge branch 'mme/mastra' of github.com:CopilotKit/CopilotKit into mme/mastra
  - make agents a dict
  - update docs
  - send tools
  - update to latest packages
  - fix problem where state sync are preventing tool calls
  - set possibly undefined toolCalls to an empty array
  - fix missing tool call ids

- 77a7457: - feat: Add Model Context Protocol (MCP) support
- d0e8a1e: - fix: fix duplicate messages on regenerate
  - @copilotkit/runtime-client-gql@1.8.5
  - @copilotkit/shared@1.8.5

## 1.8.5-next.5

### Patch Changes

- c0d3261: - full AWP support

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

  - refactor: address linter issues with the new pages

  Signed-off-by: Tyler Slaton <tyler@copilotkit.ai>

  - Merge branch 'mme/acp' into mme/mastra
  - add sse example
  - Create small-turkeys-agree.md
  - upgrade AWP
  - Merge branch 'mme/mastra' of github.com:CopilotKit/CopilotKit into mme/mastra
  - make agents a dict
  - update docs
  - send tools
  - update to latest packages
  - fix problem where state sync are preventing tool calls
  - set possibly undefined toolCalls to an empty array
  - fix missing tool call ids
  - @copilotkit/runtime-client-gql@1.8.5-next.5
  - @copilotkit/shared@1.8.5-next.5

## 1.8.5-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.5-next.4
- @copilotkit/shared@1.8.5-next.4

## 1.8.5-next.3

### Patch Changes

- 77a7457: - feat: Add Model Context Protocol (MCP) support
  - @copilotkit/runtime-client-gql@1.8.5-next.3
  - @copilotkit/shared@1.8.5-next.3

## 1.8.5-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.5-next.2
- @copilotkit/shared@1.8.5-next.2

## 1.8.5-next.1

### Patch Changes

- d0e8a1e: - fix: fix duplicate messages on regenerate
  - @copilotkit/runtime-client-gql@1.8.5-next.1
  - @copilotkit/shared@1.8.5-next.1

## 1.8.5-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.5-next.0
- @copilotkit/shared@1.8.5-next.0

## 1.8.4

### Patch Changes

- 4e28414: - use new interface properly
- Updated dependencies [f363760]
  - @copilotkit/shared@1.8.4
  - @copilotkit/runtime-client-gql@1.8.4

## 1.8.4-next.4

### Patch Changes

- 4e28414: - use new interface properly
  - @copilotkit/runtime-client-gql@1.8.4-next.4
  - @copilotkit/shared@1.8.4-next.4

## 1.8.4-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.4-next.3
- @copilotkit/shared@1.8.4-next.3

## 1.8.4-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.4-next.2
- @copilotkit/shared@1.8.4-next.2

## 1.8.4-next.1

### Patch Changes

- Updated dependencies [f363760]
  - @copilotkit/shared@1.8.4-next.1
  - @copilotkit/runtime-client-gql@1.8.4-next.1

## 1.8.4-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.4-next.0
- @copilotkit/shared@1.8.4-next.0

## 1.8.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.3
- @copilotkit/shared@1.8.3

## 1.8.3-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.3-next.0
- @copilotkit/shared@1.8.3-next.0

## 1.8.2-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.2-next.3
- @copilotkit/shared@1.8.2-next.3

## 1.8.2-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.2-next.2
- @copilotkit/shared@1.8.2-next.2

## 1.8.2-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.2-next.1
- @copilotkit/shared@1.8.2-next.1

## 1.8.2-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.2-next.0
- @copilotkit/shared@1.8.2-next.0

## 1.8.1

### Patch Changes

- 7a42944: - fix(react-core): update agentSession when agent props change #1497
  - @copilotkit/runtime-client-gql@1.8.1
  - @copilotkit/shared@1.8.1

## 1.8.1-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.1-next.1
- @copilotkit/shared@1.8.1-next.1

## 1.8.1-next.0

### Patch Changes

- 7a42944: - fix(react-core): update agentSession when agent props change #1497
  - @copilotkit/runtime-client-gql@1.8.1-next.0
  - @copilotkit/shared@1.8.1-next.0

## 1.8.0

### Patch Changes

- 73f5eaa: - fix(react-core): export missing action-related types for public API
- a50f4c1: - move default components out of ui
  - @copilotkit/runtime-client-gql@1.8.0
  - @copilotkit/shared@1.8.0

## 1.8.0-next.8

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.0-next.8
- @copilotkit/shared@1.8.0-next.8

## 1.8.0-next.7

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.0-next.7
- @copilotkit/shared@1.8.0-next.7

## 1.8.0-next.6

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.0-next.6
- @copilotkit/shared@1.8.0-next.6

## 1.8.0-next.5

### Patch Changes

- a50f4c1: - move default components out of ui
  - @copilotkit/runtime-client-gql@1.8.0-next.5
  - @copilotkit/shared@1.8.0-next.5

## 1.8.0-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.0-next.4
- @copilotkit/shared@1.8.0-next.4

## 1.8.0-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.8.0-next.3
- @copilotkit/shared@1.8.0-next.3

## 1.7.2-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.2-next.2
- @copilotkit/shared@1.7.2-next.2

## 1.7.2-next.1

### Patch Changes

- 73f5eaa: - fix(react-core): export missing action-related types for public API
  - @copilotkit/runtime-client-gql@1.7.2-next.1
  - @copilotkit/shared@1.7.2-next.1

## 1.7.2-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.2-next.0
- @copilotkit/shared@1.7.2-next.0

## 1.7.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.1
- @copilotkit/shared@1.7.1

## 1.7.1-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.1-next.0
- @copilotkit/shared@1.7.1-next.0

## 1.7.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.0
- @copilotkit/shared@1.7.0

## 1.7.0-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.0-next.1
- @copilotkit/shared@1.7.0-next.1

## 1.7.0-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.7.0-next.0
- @copilotkit/shared@1.7.0-next.0

## 1.6.0

### Minor Changes

- 7d061d9: - feat(configurable): execute langgraph with user config

### Patch Changes

- d833f4c: - fix: provide the ability to type interrupt event value
- d800f03: - fix: use memoization in useCoAgent internal functions
- 85753b3: - feat(actions): enable restricting actions to frontend only
- b454827: - fix: simplify condition options for langgraph interrupts
  - chore: add new enabled to e2e tests
  - fix: refine argument types
  - chore: document hook API reference
- c1cc77f: - feat: new useCopilotAdditionalInstructions hook and available property on useCopilotReadable
- Updated dependencies [d833f4c]
- Updated dependencies [090203d]
  - @copilotkit/runtime-client-gql@1.6.0
  - @copilotkit/shared@1.6.0

## 1.6.0-next.12

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.12
- @copilotkit/shared@1.6.0-next.12

## 1.6.0-next.11

### Patch Changes

- 85753b3: - feat(actions): enable restricting actions to frontend only
  - @copilotkit/runtime-client-gql@1.6.0-next.11
  - @copilotkit/shared@1.6.0-next.11

## 1.6.0-next.10

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.10
- @copilotkit/shared@1.6.0-next.10

## 1.6.0-next.9

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.9
- @copilotkit/shared@1.6.0-next.9

## 1.6.0-next.8

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.8
- @copilotkit/shared@1.6.0-next.8

## 1.6.0-next.7

### Patch Changes

- d800f03: - fix: use memoization in useCoAgent internal functions
  - @copilotkit/runtime-client-gql@1.6.0-next.7
  - @copilotkit/shared@1.6.0-next.7

## 1.6.0-next.6

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.6
- @copilotkit/shared@1.6.0-next.6

## 1.6.0-next.5

### Patch Changes

- Updated dependencies [090203d]
  - @copilotkit/shared@1.6.0-next.5
  - @copilotkit/runtime-client-gql@1.6.0-next.5

## 1.6.0-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.4
- @copilotkit/shared@1.6.0-next.4

## 1.6.0-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.3
- @copilotkit/shared@1.6.0-next.3

## 1.6.0-next.2

### Patch Changes

- b454827: - fix: simplify condition options for langgraph interrupts
  - chore: add new enabled to e2e tests
  - fix: refine argument types
  - chore: document hook API reference
  - @copilotkit/runtime-client-gql@1.6.0-next.2
  - @copilotkit/shared@1.6.0-next.2

## 1.6.0-next.1

### Patch Changes

- d833f4c: - fix: provide the ability to type interrupt event value
- Updated dependencies [d833f4c]
  - @copilotkit/runtime-client-gql@1.6.0-next.1
  - @copilotkit/shared@1.6.0-next.1

## 1.6.0-next.0

### Minor Changes

- 7d061d9: - feat(configurable): execute langgraph with user config

### Patch Changes

- @copilotkit/runtime-client-gql@1.6.0-next.0
- @copilotkit/shared@1.6.0-next.0

## 1.5.20

### Patch Changes

- Updated dependencies [51f0d66]
  - @copilotkit/shared@1.5.20
  - @copilotkit/runtime-client-gql@1.5.20

## 1.5.20-next.0

### Patch Changes

- Updated dependencies [51f0d66]
  - @copilotkit/shared@1.5.20-next.0
  - @copilotkit/runtime-client-gql@1.5.20-next.0

## 1.5.19

### Patch Changes

- 0dd1ab9: - fix(errors): allow non copilotkit errors to pass to consumer app error boundary
- 5bc68f8: - fix(actions): warn on action duplication
  - fix(actions): warn on coagent state render duplication
- Updated dependencies [0dd1ab9]
  - @copilotkit/shared@1.5.19
  - @copilotkit/runtime-client-gql@1.5.19

## 1.5.19-next.1

### Patch Changes

- 0dd1ab9: - fix(errors): allow non copilotkit errors to pass to consumer app error boundary
- Updated dependencies [0dd1ab9]
  - @copilotkit/shared@1.5.19-next.1
  - @copilotkit/runtime-client-gql@1.5.19-next.1

## 1.5.19-next.0

### Patch Changes

- 5bc68f8: - fix(actions): warn on action duplication
  - fix(actions): warn on coagent state render duplication
  - @copilotkit/runtime-client-gql@1.5.19-next.0
  - @copilotkit/shared@1.5.19-next.0

## 1.5.18

### Patch Changes

- f77a7b9: - fix: use warning when version mismatch is not expected to error out
- Updated dependencies [d47cd26]
- Updated dependencies [f77a7b9]
- Updated dependencies [38d3ac2]
  - @copilotkit/runtime-client-gql@1.5.18
  - @copilotkit/shared@1.5.18

## 1.5.18-next.3

### Patch Changes

- f77a7b9: - fix: use warning when version mismatch is not expected to error out
- Updated dependencies [f77a7b9]
  - @copilotkit/runtime-client-gql@1.5.18-next.3
  - @copilotkit/shared@1.5.18-next.3

## 1.5.18-next.2

### Patch Changes

- Updated dependencies [38d3ac2]
  - @copilotkit/shared@1.5.18-next.2
  - @copilotkit/runtime-client-gql@1.5.18-next.2

## 1.5.18-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.18-next.1
- @copilotkit/shared@1.5.18-next.1

## 1.5.18-next.0

### Patch Changes

- Updated dependencies [d47cd26]
  - @copilotkit/runtime-client-gql@1.5.18-next.0
  - @copilotkit/shared@1.5.18-next.0

## 1.5.17

### Patch Changes

- Updated dependencies [1fc3902]
  - @copilotkit/runtime-client-gql@1.5.17
  - @copilotkit/shared@1.5.17

## 1.5.17-next.0

### Patch Changes

- Updated dependencies [1fc3902]
  - @copilotkit/runtime-client-gql@1.5.17-next.0
  - @copilotkit/shared@1.5.17-next.0

## 1.5.16

### Patch Changes

- 07be5ca: - fix: disable error toasts if dev console is disabled
- Updated dependencies [48b7c7b]
  - @copilotkit/runtime-client-gql@1.5.16
  - @copilotkit/shared@1.5.16

## 1.5.16-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.16-next.2
- @copilotkit/shared@1.5.16-next.2

## 1.5.16-next.1

### Patch Changes

- Updated dependencies [48b7c7b]
  - @copilotkit/runtime-client-gql@1.5.16-next.1
  - @copilotkit/shared@1.5.16-next.1

## 1.5.16-next.0

### Patch Changes

- 07be5ca: - fix: disable error toasts if dev console is disabled
  - @copilotkit/runtime-client-gql@1.5.16-next.0
  - @copilotkit/shared@1.5.16-next.0

## 1.5.15

### Patch Changes

- 06f9f35: - feat(interrupt): add copilotkit interrupt as messages with copilotkit interrupt convenience fn
  - chore(deps): update dependencies for demos
  - chore(interrupt-as-message): add e2e test for interrupt as message
- 7b3141d: - feat(interrupt): support LG interrupt with useLangGraphInterrupt hook
  - chore(interrupt): add e2e test to interrupt functionality
  - feat(interrupt): add support for multiple interrupts and conditions
- c9ae305: - perf: prevent redundant API calls
- Updated dependencies [0dc0f43]
- Updated dependencies [06f9f35]
- Updated dependencies [7b3141d]
- Updated dependencies [0bbb4ab]
  - @copilotkit/runtime-client-gql@1.5.15
  - @copilotkit/shared@1.5.15

## 1.5.15-next.8

### Patch Changes

- 06f9f35: - feat(interrupt): add copilotkit interrupt as messages with copilotkit interrupt convenience fn
  - chore(deps): update dependencies for demos
  - chore(interrupt-as-message): add e2e test for interrupt as message
- Updated dependencies [06f9f35]
  - @copilotkit/runtime-client-gql@1.5.15-next.8
  - @copilotkit/shared@1.5.15-next.8

## 1.5.15-next.7

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.15-next.7
- @copilotkit/shared@1.5.15-next.7

## 1.5.15-next.6

### Patch Changes

- c9ae305: - perf: prevent redundant API calls
  - @copilotkit/runtime-client-gql@1.5.15-next.6
  - @copilotkit/shared@1.5.15-next.6

## 1.5.15-next.5

### Patch Changes

- Updated dependencies [0dc0f43]
  - @copilotkit/runtime-client-gql@1.5.15-next.5
  - @copilotkit/shared@1.5.15-next.5

## 1.5.15-next.4

### Patch Changes

- 7b3141d: - feat(interrupt): support LG interrupt with useLangGraphInterrupt hook
  - chore(interrupt): add e2e test to interrupt functionality
  - feat(interrupt): add support for multiple interrupts and conditions
- Updated dependencies [7b3141d]
  - @copilotkit/runtime-client-gql@1.5.15-next.4
  - @copilotkit/shared@1.5.15-next.4

## 1.5.15-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.15-next.3
- @copilotkit/shared@1.5.15-next.3

## 1.5.15-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.15-next.2
- @copilotkit/shared@1.5.15-next.2

## 1.5.15-next.1

### Patch Changes

- Updated dependencies [0bbb4ab]
  - @copilotkit/runtime-client-gql@1.5.15-next.1
  - @copilotkit/shared@1.5.15-next.1

## 1.5.15-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.15-next.0
- @copilotkit/shared@1.5.15-next.0

## 1.5.14

### Patch Changes

- 0061f65: - feat: allows dev mode for cloud onboarding flow
- Updated dependencies [0061f65]
  - @copilotkit/shared@1.5.14
  - @copilotkit/runtime-client-gql@1.5.14

## 1.5.14-next.0

### Patch Changes

- 0061f65: - feat: allows dev mode for cloud onboarding flow
- Updated dependencies [0061f65]
  - @copilotkit/shared@1.5.14-next.0
  - @copilotkit/runtime-client-gql@1.5.14-next.0

## 1.5.13

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.13
- @copilotkit/shared@1.5.13

## 1.5.13-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.13-next.0
- @copilotkit/shared@1.5.13-next.0

## 1.5.12

### Patch Changes

- 926499b: - Load the previous state of an agent if `threadId` is provided to CopilotKit, including all messages
- 6136a57: - fix(errors): add custom error classes to better describe library errors
  - fix(errors): use new errors in error handling
  - chore: add documentation and links to respective errors
- cb43c05: - fix: set up managed LLM retries and report error to render method
- Updated dependencies [fb87bcf]
- Updated dependencies [926499b]
- Updated dependencies [6136a57]
  - @copilotkit/runtime-client-gql@1.5.12
  - @copilotkit/shared@1.5.12

## 1.5.12-next.7

### Patch Changes

- 926499b: - Load the previous state of an agent if `threadId` is provided to CopilotKit, including all messages
- Updated dependencies [926499b]
  - @copilotkit/runtime-client-gql@1.5.12-next.7
  - @copilotkit/shared@1.5.12-next.7

## 1.5.12-next.6

### Patch Changes

- 6136a57: - fix(errors): add custom error classes to better describe library errors
  - fix(errors): use new errors in error handling
  - chore: add documentation and links to respective errors
- Updated dependencies [6136a57]
  - @copilotkit/runtime-client-gql@1.5.12-next.6
  - @copilotkit/shared@1.5.12-next.6

## 1.5.12-next.5

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.12-next.5
- @copilotkit/shared@1.5.12-next.5

## 1.5.12-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.12-next.4
- @copilotkit/shared@1.5.12-next.4

## 1.5.12-next.3

### Patch Changes

- cb43c05: - fix: set up managed LLM retries and report error to render method
  - @copilotkit/runtime-client-gql@1.5.12-next.3
  - @copilotkit/shared@1.5.12-next.3

## 1.5.12-next.2

### Patch Changes

- Updated dependencies [fb87bcf]
  - @copilotkit/runtime-client-gql@1.5.12-next.2
  - @copilotkit/shared@1.5.12-next.2

## 1.5.12-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.12-next.1
- @copilotkit/shared@1.5.12-next.1

## 1.5.12-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.12-next.0
- @copilotkit/shared@1.5.12-next.0

## 1.5.11

### Patch Changes

- db3d539: test release notes
- e5d588d: test changelog
- 4211318: test changelog
- d431537: Test release notes
- Updated dependencies [72f9e58]
- Updated dependencies [aecb6f4]
- Updated dependencies [0a2e07e]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.11
  - @copilotkit/shared@1.5.11

## 1.5.11-next.0

### Patch Changes

- db3d539: test release notes
- e5d588d: test changelog
- 4211318: test changelog
- d431537: Test release notes
- Updated dependencies [72f9e58]
- Updated dependencies [aecb6f4]
- Updated dependencies [0a2e07e]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.11-next.0
  - @copilotkit/shared@1.5.11-next.0

## 1.5.10

### Patch Changes

- db3d539: test release notes
- e5d588d: test changelog
- 4211318: test changelog
- d431537: Test release notes
- Updated dependencies [72f9e58]
- Updated dependencies [aecb6f4]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.10
  - @copilotkit/shared@1.5.10

## 1.5.10-next.0

### Patch Changes

- db3d539: test release notes
- e5d588d: test changelog
- 4211318: test changelog
- d431537: Test release notes
- Updated dependencies [72f9e58]
- Updated dependencies [aecb6f4]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.10-next.0
  - @copilotkit/shared@1.5.10-next.0

## 1.5.9

### Patch Changes

- db3d539: test release notes
- e5d588d: test changelog
- 4211318: test changelog
- d431537: Test release notes
- Updated dependencies [72f9e58]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.9
  - @copilotkit/shared@1.5.9

## 1.5.8

### Patch Changes

- db3d539: test release notes
- e5d588d: test changelog
- 4211318: test changelog
- d431537: Test release notes
- Updated dependencies [72f9e58]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.8
  - @copilotkit/shared@1.5.8

## 1.5.6-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.6-next.0
- @copilotkit/shared@1.5.6-next.0

## 1.5.5-next.5

### Patch Changes

- db3d539: test release notes
  - @copilotkit/runtime-client-gql@1.5.5-next.5
  - @copilotkit/shared@1.5.5-next.5

## 1.5.5-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.5-next.3
- @copilotkit/shared@1.5.5-next.3

## 1.5.5-next.2

### Patch Changes

- Updated dependencies [72f9e58]
- Updated dependencies [9b3bdc2]
  - @copilotkit/runtime-client-gql@1.5.5-next.2
  - @copilotkit/shared@1.5.5-next.2

## 1.5.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.4
- @copilotkit/shared@1.5.4

## 1.5.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.5.3
- @copilotkit/shared@1.5.3

## 1.5.2

### Patch Changes

- Updated dependencies [b0192c1]
  - @copilotkit/runtime-client-gql@1.5.2
  - @copilotkit/shared@1.5.2

## 1.5.1

### Patch Changes

- 5c01e9e: test prerelease #4
- ed39d40: - [CPK-1034] adds `useCopilotAuthenticatedAction`
- da280ed: Test prerelease script
- 27e42d7: testing a prerelease
- 05240a9: test pre #2
- 33218fe: test prerelease #3
- 03f3d6f: Test next prerelease
- 649ebcc: - fix: add warning when using agents that are not available on agent related hooks
- 6dfa0d2: - feat: add temperature parameter support for LLM completions
- Updated dependencies [5c01e9e]
- Updated dependencies [da280ed]
- Updated dependencies [27e42d7]
- Updated dependencies [05240a9]
- Updated dependencies [33218fe]
- Updated dependencies [03f3d6f]
- Updated dependencies [649ebcc]
  - @copilotkit/runtime-client-gql@1.5.1
  - @copilotkit/shared@1.5.1

## 1.5.1-next.3

### Patch Changes

- 33218fe: test prerelease #3
- Updated dependencies [33218fe]
  - @copilotkit/runtime-client-gql@1.5.1-next.3
  - @copilotkit/shared@1.5.1-next.3

## 1.5.1-next.2

### Patch Changes

- ed39d40: - [CPK-1034] adds `useCopilotAuthenticatedAction`
- da280ed: Test prerelease script
- 649ebcc: - fix: add warning when using agents that are not available on agent related hooks
- Updated dependencies [da280ed]
- Updated dependencies [649ebcc]
  - @copilotkit/runtime-client-gql@1.5.1-next.2
  - @copilotkit/shared@1.5.1-next.2

## 1.5.1-next.1

### Patch Changes

- 03f3d6f: Test next prerelease
- Updated dependencies [03f3d6f]
  - @copilotkit/runtime-client-gql@1.5.1-next.1
  - @copilotkit/shared@1.5.1-next.1

## 1.5.1-next.0

### Patch Changes

- 27e42d7: testing a prerelease
- 6dfa0d2: - feat: add temperature parameter support for LLM completions
- Updated dependencies [27e42d7]
  - @copilotkit/runtime-client-gql@1.5.1-next.0
  - @copilotkit/shared@1.5.1-next.0

## 1.5.0

### Minor Changes

- 1b47092: Synchronize LangGraph messages with CopilotKit

### Patch Changes

- 00e9488: - fix: wait for renderAndWaitForResponse handler to be ready before rendering
- 1b47092: CoAgents v0.3 prerelease
- Updated dependencies [1b47092]
- Updated dependencies [1b47092]
  - @copilotkit/runtime-client-gql@1.5.0
  - @copilotkit/shared@1.5.0

## 1.5.0-coagents-v0-3.0

### Minor Changes

- Synchronize LangGraph messages with CopilotKit

### Patch Changes

- e66bce4: CoAgents v0.3 prerelease
- Updated dependencies
- Updated dependencies [e66bce4]
  - @copilotkit/runtime-client-gql@1.5.0-coagents-v0-3.0
  - @copilotkit/shared@1.5.0-coagents-v0-3.0

## 1.4.8

### Patch Changes

- - Better error handling
  - Introduce new "EmptyLLMAdapter" for when using CoAgents
  - Improve dev console help options
  - Allow CopilotKit remote endpoint without agents
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.8
  - @copilotkit/shared@1.4.8

## 1.4.8-next.0

### Patch Changes

- @copilotkit/runtime-client-gql@1.4.8-next.0
- @copilotkit/shared@1.4.8-next.0

## 1.4.7

### Patch Changes

- Fix broken build script before release
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.7
  - @copilotkit/shared@1.4.7

## 1.4.6

### Patch Changes

- .

## 1.4.5

### Patch Changes

- testing release workflow
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.5
  - @copilotkit/shared@1.4.5

## 1.4.5-next.0

### Patch Changes

- testing release workflow
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.5-next.0
  - @copilotkit/shared@1.4.5-next.0

## 1.4.4

### Patch Changes

- e35e6ad: - test
  - update config.json
  - Merge remote-tracking branch 'origin/main' into feat/test-changeset-bot-1
  - test
  - test
  - @copilotkit/runtime-client-gql@1.4.4
  - @copilotkit/shared@1.4.4

## 1.4.4-next.4

### Patch Changes

- @copilotkit/runtime-client-gql@1.4.4-next.4
- @copilotkit/shared@1.4.4-next.4

## 1.4.4-next.3

### Patch Changes

- @copilotkit/runtime-client-gql@1.4.4-next.3
- @copilotkit/shared@1.4.4-next.3

## 1.4.4-next.2

### Patch Changes

- @copilotkit/runtime-client-gql@1.4.4-next.2
- @copilotkit/shared@1.4.4-next.2

## 1.4.4-next.1

### Patch Changes

- @copilotkit/runtime-client-gql@1.4.4-next.1
- @copilotkit/shared@1.4.4-next.1

## 1.4.4-next.0

### Patch Changes

- e35e6ad: - test
  - update config.json
  - Merge remote-tracking branch 'origin/main' into feat/test-changeset-bot-1
  - test
  - test
  - @copilotkit/runtime-client-gql@1.4.4-next.0
  - @copilotkit/shared@1.4.4-next.0

## 1.4.3

### Patch Changes

- c296282: - Better error surfacing when using LangGraph Platform streaming
  - Ensure state is immediately set without using flushSync
- - Better error surfacing when using LangGraph Platform streaming
  - Ensure state is immediately set without using flushSync
- Updated dependencies [c296282]
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.3
  - @copilotkit/shared@1.4.3

## 1.4.3-pre.0

### Patch Changes

- - Better error surfacing when using LangGraph Platform streaming
  - Ensure state is immediately set without using flushSync
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.3-pre.0
  - @copilotkit/shared@1.4.3-pre.0

## 1.4.2

### Patch Changes

- - Make sure agent state is set immediately (#1077)
  - Support running an agent without messages (#1075)
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.2
  - @copilotkit/shared@1.4.2

## 1.4.1

### Patch Changes

- 1721cbd: lower case copilotkit property
- 1721cbd: add zod conversion
- 8d0144f: bump
- 8d0144f: bump
- 8d0144f: bump
- e16d95e: New prerelease
- 1721cbd: Add convertActionsToDynamicStructuredTools to sdk-js
- CopilotKit Core:

  - Improved error messages and overall logs
  - `useCopilotAction.renderAndAwait` renamed to `.renderAndAwaitForResponse` (backwards compatible, will be deprecated in the future)
  - Improved scrolling behavior. It is now possible to scroll up during LLM response generation
  - Added Azure OpenAI integration
  - Updated interfaces for better developer ergonomics

  CoAgents:

  - Renamed `remoteActions` to `remoteEndpoints` (backwards compatible, will be deprecated in the future)
  - Support for LangGraph Platform in Remote Endpoints
  - LangGraph JS Support for CoAgents (locally via `langgraph dev`, `langgraph up` or deployed to LangGraph Platform)
  - Improved LangSmith integration - requests made through CoAgents will now surface in LangSmith
  - Enhanced state management and message handling

  CopilotKid Back-end SDK:

  - Released a whole-new `@copilotkit/sdk-js` for building agents with LangGraph JS Support

- 8d0144f: bump
- 8d0144f: bump
- fef1b74: fix assistant message CSS and propagate actions to LG JS
- Updated dependencies [1721cbd]
- Updated dependencies [1721cbd]
- Updated dependencies [8d0144f]
- Updated dependencies [8d0144f]
- Updated dependencies [8d0144f]
- Updated dependencies [e16d95e]
- Updated dependencies [1721cbd]
- Updated dependencies
- Updated dependencies [8d0144f]
- Updated dependencies [8d0144f]
- Updated dependencies [fef1b74]
  - @copilotkit/runtime-client-gql@1.4.1
  - @copilotkit/shared@1.4.1

## 1.4.1-pre.6

### Patch Changes

- 1721cbd: lower case copilotkit property
- 1721cbd: add zod conversion
- 1721cbd: Add convertActionsToDynamicStructuredTools to sdk-js
- fix assistant message CSS and propagate actions to LG JS
- Updated dependencies [1721cbd]
- Updated dependencies [1721cbd]
- Updated dependencies [1721cbd]
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.6
  - @copilotkit/shared@1.4.1-pre.6

## 1.4.1-pre.5

### Patch Changes

- bump
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.5
  - @copilotkit/shared@1.4.1-pre.5

## 1.4.1-pre.4

### Patch Changes

- bump
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.4
  - @copilotkit/shared@1.4.1-pre.4

## 1.4.1-pre.3

### Patch Changes

- bump
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.3
  - @copilotkit/shared@1.4.1-pre.3

## 1.4.1-pre.2

### Patch Changes

- bump
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.2
  - @copilotkit/shared@1.4.1-pre.2

## 1.4.1-pre.1

### Patch Changes

- bump
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.1
  - @copilotkit/shared@1.4.1-pre.1

## 1.4.1-pre.0

### Patch Changes

- New prerelease
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.4.1-pre.0
  - @copilotkit/shared@1.4.1-pre.0

## 1.4.0

### Minor Changes

CopilotKit Core:

- Improved error messages and overall logs
- `useCopilotAction.renderAndAwait` renamed to `.renderAndAwaitForResponse` (backwards compatible, will be deprecated in the future)
- Improved scrolling behavior. It is now possible to scroll up during LLM response generation
- Added Azure OpenAI integration
- Updated interfaces for better developer ergonomics

CoAgents:

- Renamed `remoteActions` to `remoteEndpoints` (backwards compatible, will be deprecated in the future)
- Support for LangGraph Platform in Remote Endpoints
- LangGraph JS Support for CoAgents (locally via `langgraph dev`, `langgraph up` or deployed to LangGraph Platform)
- Improved LangSmith integration - requests made through CoAgents will now surface in LangSmith
- Enhanced state management and message handling

CopilotKid Back-end SDK:

- Released a whole-new `@copilotkit/sdk-js` for building agents with LangGraph JS Support

### Patch Changes

- f6fab28: update tsup config
- f6fab28: update entry
- f6fab28: export langchain module
- 8a77944: Improve LangSmith support
- f6fab28: Ensure intermediate state config is sent as snake case
- f6fab28: update entry in tsup config
- 8a77944: Ensure the last message is sent to LangSmith
- a5efccd: Revert rxjs changes
- f6fab28: update entry
- f6fab28: Update exports
- f6fab28: Update exports
- 332d744: Add support for Azure OpenAI
- f6fab28: Export LangGraph functions
- f6fab28: Update lockfile
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies
- Updated dependencies [f6fab28]
- Updated dependencies [8a77944]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [8a77944]
- Updated dependencies [a5efccd]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [332d744]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
  - @copilotkit/runtime-client-gql@1.4.0
  - @copilotkit/shared@1.4.0

## 1.3.16-mme-revert-rxjs-changes.10

### Patch Changes

- f6fab28: update tsup config
- f6fab28: update entry
- f6fab28: export langchain module
- 8a77944: Improve LangSmith support
- f6fab28: Ensure intermediate state config is sent as snake case
- f6fab28: update entry in tsup config
- 8a77944: Ensure the last message is sent to LangSmith
- Revert rxjs changes
- f6fab28: update entry
- f6fab28: Update exports
- f6fab28: Update exports
- 332d744: Add support for Azure OpenAI
- f6fab28: Export LangGraph functions
- f6fab28: Update lockfile
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [8a77944]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [8a77944]
- Updated dependencies
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
- Updated dependencies [332d744]
- Updated dependencies [f6fab28]
- Updated dependencies [f6fab28]
  - @copilotkit/runtime-client-gql@1.3.16-mme-revert-rxjs-changes.10
  - @copilotkit/shared@1.3.16-mme-revert-rxjs-changes.10

## 1.3.15

### Patch Changes

- pass description for array and object action parameters in langchain adapter
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.15
  - @copilotkit/shared@1.3.15

## 1.3.14

### Patch Changes

- Add data-test-id to some elements for testing
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.14
  - @copilotkit/shared@1.3.14

## 1.3.13

### Patch Changes

- fix usage of one-at-a-time tool when called multiple times
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.13
  - @copilotkit/shared@1.3.13

## 1.3.12

### Patch Changes

- - enable dynamic parameters in langchain adapter tool call
  - fix unparsable action arguments causing tool call crashes
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.12
  - @copilotkit/shared@1.3.12

## 1.3.11

### Patch Changes

- 08e8956: Fix duplicate messages
- Fix duplicate messages
- Updated dependencies [08e8956]
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.11
  - @copilotkit/shared@1.3.11

## 1.3.11-mme-fix-duplicate-messages.0

### Patch Changes

- Fix duplicate messages
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.11-mme-fix-duplicate-messages.0
  - @copilotkit/shared@1.3.11-mme-fix-duplicate-messages.0

## 1.3.10

### Patch Changes

- change how message chunk type is resolved (fixed langchain adapters)
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.10
  - @copilotkit/shared@1.3.10

## 1.3.9

### Patch Changes

- Fix message id issues
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.9
  - @copilotkit/shared@1.3.9

## 1.3.8

### Patch Changes

- fix textarea on multiple llm providers and memoize react ui context
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.8
  - @copilotkit/shared@1.3.8

## 1.3.7

### Patch Changes

- Fix libraries for React 19 and Next.js 15 support
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.7
  - @copilotkit/shared@1.3.7

## 1.3.6

### Patch Changes

- 1. Removes the usage of the `crypto` Node pacakge, instaed uses `uuid`. This ensures that non-Next.js React apps can use CopilotKit.
  2. Fixes Nest.js runtime docs

- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.6
  - @copilotkit/shared@1.3.6

## 1.3.5

### Patch Changes

- Improve CoAgent state render
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.5
  - @copilotkit/shared@1.3.5

## 1.3.4

### Patch Changes

- Add followUp property to useCopilotAction
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.4
  - @copilotkit/shared@1.3.4

## 1.3.3

### Patch Changes

- Impvovements to error handling and CoAgent protocol
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.3
  - @copilotkit/shared@1.3.3

## 1.3.2

### Patch Changes

- Features and bug fixes
- 30232c0: Ensure actions can be discovered on state change
- Updated dependencies
- Updated dependencies [30232c0]
  - @copilotkit/runtime-client-gql@1.3.2
  - @copilotkit/shared@1.3.2

## 1.3.2-mme-discover-actions.0

### Patch Changes

- Ensure actions can be discovered on state change
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.2-mme-discover-actions.0
  - @copilotkit/shared@1.3.2-mme-discover-actions.0

## 1.3.1

### Patch Changes

- Revert CSS injection
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.3.1
  - @copilotkit/shared@1.3.1

## 1.3.0

### Minor Changes

- CoAgents and remote actions

### Patch Changes

- 5b63f55: stream intermediate state
- b6fd3d8: Better message grouping
- 89420c6: Rename hooks and bugfixes
- b6e8824: useCoAgent/useCoAgentAction
- 91c35b9: useAgentState
- 00be203: Remote actions preview
- fb15f72: Reduce request size by skipping intermediate state
- 8ecc3e4: Fix useCoAgent start/stop bug
- Updated dependencies
- Updated dependencies [5b63f55]
- Updated dependencies [b6fd3d8]
- Updated dependencies [89420c6]
- Updated dependencies [b6e8824]
- Updated dependencies [91c35b9]
- Updated dependencies [00be203]
- Updated dependencies [fb15f72]
- Updated dependencies [8ecc3e4]
  - @copilotkit/runtime-client-gql@1.3.0
  - @copilotkit/shared@1.3.0

## 1.2.1

### Patch Changes

- inject minified css in bundle

  - removes the need to import `styles.css` manually
  - empty `styles.css` included in the build for backwards compatibility
  - uses tsup's `injectStyles` with `postcss` to bundle and minify the CSS, then inject it as a style tag
  - currently uses my fork of `tsup` where I added support for async function in `injectStyles` (must-have for postcss), a PR from my fork to the main library will follow shortly
  - remove material-ui, and use `react-icons` for icons (same icons as before)
  - remove unused `IncludedFilesPreview` component
  - updated docs

- Updated dependencies
  - @copilotkit/runtime-client-gql@1.2.1
  - @copilotkit/shared@1.2.1

## 1.2.0

### Minor Changes

- Fix errors related to crypto not being found, and other bug fixes

### Patch Changes

- 638d51d: appendMessage fix 1
- faccbe1: state-abuse resistance for useCopilotChat
- b0cf700: remove unnecessary logging
- Updated dependencies
- Updated dependencies [638d51d]
- Updated dependencies [faccbe1]
- Updated dependencies [b0cf700]
  - @copilotkit/runtime-client-gql@1.2.0
  - @copilotkit/shared@1.2.0

## 1.1.2

### Patch Changes

- Pin headless-ui/react version to v2.1.1
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.1.2
  - @copilotkit/shared@1.1.2

## 1.1.1

### Patch Changes

- - improved documentation
  - center textarea popup
  - show/hide dev console
  - forward maxTokens, stop and force function calling
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.1.1
  - @copilotkit/shared@1.1.1

## 1.1.0

### Minor Changes

- Official support for Groq (`GroqAdapter`)

### Patch Changes

- Updated dependencies
  - @copilotkit/runtime-client-gql@1.1.0
  - @copilotkit/shared@1.1.0

## 1.0.9

### Patch Changes

- Dev console, bugfixes
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.9
  - @copilotkit/shared@1.0.9

## 1.0.8

### Patch Changes

- Remove redundant console logs
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.8
  - @copilotkit/shared@1.0.8

## 1.0.7

### Patch Changes

- Add \_copilotkit internal properties to runtime
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.7
  - @copilotkit/shared@1.0.7

## 1.0.6

### Patch Changes

- - Proactively prevent race conditions
  - Improve token counting performance
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.6
  - @copilotkit/shared@1.0.6

## 1.0.5

### Patch Changes

- Include @copilotkit/runtime-client-gql NPM package version in request to Runtime
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.5
  - @copilotkit/shared@1.0.5

## 1.0.4

### Patch Changes

- Remove nanoid
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.4
  - @copilotkit/shared@1.0.4

## 1.0.3

### Patch Changes

- Add README.md to published packages and add keywords to package.json
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.3
  - @copilotkit/shared@1.0.3

## 1.0.2

### Patch Changes

- Add README.md and homepage/url to published packages
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.2
  - @copilotkit/shared@1.0.2

## 1.0.1

### Patch Changes

- Remove PostHog, use Segment Anonymous Telemetry instead
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.1
  - @copilotkit/shared@1.0.1

## 1.0.0

### Major Changes

- b6a4b6eb: V1.0 Release Candidate

  - A robust new protocol between the frontend and the Copilot Runtime
  - Support for Copilot Cloud
  - Generative UI
  - Support for LangChain universal tool calling
  - OpenAI assistant API streaming

- V1.0 Release

  - A robust new protocol between the frontend and the Copilot Runtime
  - Support for Copilot Cloud
  - Generative UI
  - Support for LangChain universal tool calling
  - OpenAI assistant API streaming

### Patch Changes

- b6a4b6eb: Introduce anonymous telemetry
- b6a4b6eb: Set default Copilot Cloud runtime URL to versioned URL (v1)
- Updated dependencies [b6a4b6eb]
- Updated dependencies [b6a4b6eb]
- Updated dependencies [b6a4b6eb]
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.0
  - @copilotkit/shared@1.0.0

## 1.0.0-beta.2

### Patch Changes

- Set default Copilot Cloud runtime URL to versioned URL (v1)
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.0-beta.2
  - @copilotkit/shared@1.0.0-beta.2

## 1.0.0-beta.1

### Patch Changes

- Introduce anonymous telemetry
- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.0-beta.1
  - @copilotkit/shared@1.0.0-beta.1

## 1.0.0-beta.0

### Major Changes

- V1.0 Release Candidate

  - A robust new protocol between the frontend and the Copilot Runtime
  - Support for Copilot Cloud
  - Generative UI
  - Support for LangChain universal tool calling
  - OpenAI assistant API streaming

### Patch Changes

- Updated dependencies
  - @copilotkit/runtime-client-gql@1.0.0-beta.0
  - @copilotkit/shared@1.0.0-beta.0

## 0.37.0

### Minor Changes

- f771353: Fix: Stale CopilotReadable
- 9df8d43: Remove unneeded tailwind components
- CSS improvements, useCopilotChat, invisible messages

### Patch Changes

- Updated dependencies [f771353]
- Updated dependencies [9df8d43]
- Updated dependencies
  - @copilotkit/shared@0.37.0

## 0.37.0-mme-fix-textarea-css.1

### Minor Changes

- Remove unneeded tailwind components

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.37.0-mme-fix-textarea-css.1

## 0.37.0-mme-fix-feedback-readable.0

### Minor Changes

- Fix: Stale CopilotReadable

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.37.0-mme-fix-feedback-readable.0

## 0.36.0

### Minor Changes

- 8baa862: Add push to talk prototype
- chat suggestions, standalone chat component, gemini adapter, push to talk

### Patch Changes

- Updated dependencies [8baa862]
- Updated dependencies
  - @copilotkit/shared@0.36.0

## 0.36.0-mme-push-to-talk.0

### Minor Changes

- Add push to talk prototype

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.36.0-mme-push-to-talk.0

## 0.25.0

### Minor Changes

- 718520b: gpt-4-turbo-april-2024 function calling fixes
- 95bcbd8: streamline cloud configuration
- 95bcbd8: Rename
- 95bcbd8: Upgrade langchain
- 95bcbd8: Support input guardrails (cloud)
- 95bcbd8: Unify api key handling
- CopilotCloud V1, useCopilotReadable and more...
- 95bcbd8: Get api key from headers dict
- 95bcbd8: Update comments
- 95bcbd8: Include reason in guardrails response
- 718520b: gpt-4-turbo-april-2024
- 95bcbd8: Update comments
- 5f6f57a: fix backend function calling return values
- 95bcbd8: Retrieve public API key

### Patch Changes

- Updated dependencies [718520b]
- Updated dependencies [95bcbd8]
- Updated dependencies [95bcbd8]
- Updated dependencies [95bcbd8]
- Updated dependencies [95bcbd8]
- Updated dependencies [95bcbd8]
- Updated dependencies
- Updated dependencies [95bcbd8]
- Updated dependencies [95bcbd8]
- Updated dependencies [95bcbd8]
- Updated dependencies [718520b]
- Updated dependencies [95bcbd8]
- Updated dependencies [5f6f57a]
- Updated dependencies [95bcbd8]
  - @copilotkit/shared@0.9.0

## 0.25.0-mme-cloud.7

### Minor Changes

- Get api key from headers dict

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-mme-cloud.7

## 0.25.0-mme-cloud.6

### Minor Changes

- Upgrade langchain

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-mme-cloud.6

## 0.25.0-mme-cloud.5

### Minor Changes

- Update comments

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-mme-cloud.5

## 0.25.0-mme-cloud.4

### Minor Changes

- Update comments

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-mme-cloud.4

## 0.25.0-mme-cloud.3

### Minor Changes

- 85c029b: streamline cloud configuration
- Rename
- a5ade3b: Support input guardrails (cloud)
- 12ff590: Unify api key handling
- f0c4745: Include reason in guardrails response
- 17f4b1b: Retrieve public API key

### Patch Changes

- Updated dependencies [85c029b]
- Updated dependencies
- Updated dependencies [a5ade3b]
- Updated dependencies [12ff590]
- Updated dependencies [f0c4745]
- Updated dependencies [17f4b1b]
  - @copilotkit/shared@0.9.0-mme-cloud.3

## 0.25.0-function-calling-fixes.2

### Minor Changes

- fix backend function calling return values

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-function-calling-fixes.2

## 0.25.0-function-calling-fixes.1

### Minor Changes

- gpt-4-turbo-april-2024 function calling fixes

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-function-calling-fixes.1

## 0.25.0-alpha.0

### Minor Changes

- gpt-4-turbo-april-2024

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.9.0-alpha.0

## 0.24.0

### Minor Changes

- 1f06d29: declare esm/cjs/types in export
- fix esm error
- 5a0b2cf: Inline codeblock style to avoid ESM error
- e12b921: ESM by default

### Patch Changes

- Updated dependencies [1f06d29]
- Updated dependencies
- Updated dependencies [5a0b2cf]
- Updated dependencies [e12b921]
  - @copilotkit/shared@0.8.0

## 0.24.0-mme-esm-error.2

### Minor Changes

- Inline codeblock style to avoid ESM error

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.8.0-mme-esm-error.2

## 0.24.0-mme-esm-error.1

### Minor Changes

- declare esm/cjs/types in export

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.8.0-mme-esm-error.1

## 0.24.0-mme-esm-error.0

### Minor Changes

- ESM by default

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.8.0-mme-esm-error.0

## 0.23.0

### Minor Changes

- 899aa6e: Backend improvements for running on GCP
- Improve streamHttpServerResponse for express and firebase apps

### Patch Changes

- Updated dependencies [899aa6e]
- Updated dependencies
  - @copilotkit/shared@0.7.0

## 0.23.0-mme-firebase-fixes.0

### Minor Changes

- Backend improvements for running on GCP

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.7.0-mme-firebase-fixes.0

## 0.22.0

### Minor Changes

- Improve Next.js support and action rendering

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.6.0

## 0.21.0

### Minor Changes

- c4010e7: Pre Release
- be00d61: Alpha
- ec8481c: Alpha
- 3fbee5d: OpenAIAdapter-getter
- e09dc44: Test backward compatibility of AnnotatedFunction on the backend
- 3f5ad60: OpenAIAdapter: make openai instance gettable
- 0dd6180: QA
- 225812d: QA new action type
- New actions: custom chat components, and typed arguments

### Patch Changes

- Updated dependencies [c4010e7]
- Updated dependencies [be00d61]
- Updated dependencies [ec8481c]
- Updated dependencies [3fbee5d]
- Updated dependencies [e09dc44]
- Updated dependencies [3f5ad60]
- Updated dependencies [0dd6180]
- Updated dependencies [225812d]
- Updated dependencies
  - @copilotkit/shared@0.5.0

## 0.21.0-mme-deprecate-annotated-function.4

### Minor Changes

- Test backward compatibility of AnnotatedFunction on the backend

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.5.0-mme-deprecate-annotated-function.4

## 0.21.0-mme-pre-release.3

### Minor Changes

- Pre Release
- 3fbee5d: OpenAIAdapter-getter
- 3f5ad60: OpenAIAdapter: make openai instance gettable

### Patch Changes

- Updated dependencies
- Updated dependencies [3fbee5d]
- Updated dependencies [3f5ad60]
  - @copilotkit/shared@0.5.0-mme-pre-release.3

## 0.21.0-mme-function-call-labels.2

### Minor Changes

- be00d61: Alpha
- QA

### Patch Changes

- Updated dependencies [be00d61]
- Updated dependencies
  - @copilotkit/shared@0.5.0-mme-function-call-labels.2

## 0.21.0-mme-experimental-actions.1

### Minor Changes

- Alpha

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.5.0-mme-experimental-actions.1

## 0.21.0-mme-experimental-actions.0

### Minor Changes

- QA new action type

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.5.0-mme-experimental-actions.0

## 0.20.1

### Patch Changes

- 5ec8ad4: fix- bring back removeBackendOnlyProps
- 5a154d0: fix: bring back removeBackendOnlyProps
- fix: bring back removeBackendOnlyProps
- Updated dependencies [5ec8ad4]
- Updated dependencies [5a154d0]
- Updated dependencies
  - @copilotkit/shared@0.4.1

## 0.20.1-atai-0223-fix-backendOnlyProps.1

### Patch Changes

- fix- bring back removeBackendOnlyProps
- Updated dependencies
  - @copilotkit/shared@0.4.1-atai-0223-fix-backendOnlyProps.1

## 0.20.1-atai-0223-fix-backendOnlyProps.0

### Patch Changes

- fix: bring back removeBackendOnlyProps
- Updated dependencies
  - @copilotkit/shared@0.4.1-atai-0223-fix-backendOnlyProps.0

## 0.20.0

### Minor Changes

- CopilotTask, function return values, LangChain support, LangServe support
- 401e474: Test the tools API
- 2f3296e: Test automation

### Patch Changes

- Updated dependencies
- Updated dependencies [401e474]
- Updated dependencies [2f3296e]
  - @copilotkit/shared@0.4.0

## 0.20.0-beta-automation.1

### Minor Changes

- Test automation

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.4.0-beta-automation.1

## 0.20.0-tools.0

### Minor Changes

- Test the tools API

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.4.0-tools.0

## 0.19.0

### Minor Changes

- node CopilotBackend support
- 58a8524: clean node example impl
- a34a226: node-native backend support

### Patch Changes

- Updated dependencies
- Updated dependencies [58a8524]
- Updated dependencies [a34a226]
  - @copilotkit/shared@0.3.0

## 0.19.0-alpha.1

### Minor Changes

- clean node example impl

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.3.0-alpha.1

## 0.19.0-alpha.0

### Minor Changes

- node-native backend support

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.3.0-alpha.0

## 0.18.0

### Minor Changes

- eba87c7: .4
- 29ee27e: New Copilot ui
- 61168c7: no treeshake
- fb32fe3: .2
- eba87c7: .3
- new chatbot ui, new component names, new build system, new docs
- 61168c7: no treeshake take 2
- 61168c7: remove treeshake in build
- fb32fe3: build naming refactor
- eba87c7: .5
- 61168c7: cache clean
- fb32fe3: .3

### Patch Changes

- Updated dependencies [eba87c7]
- Updated dependencies [61168c7]
- Updated dependencies [fb32fe3]
- Updated dependencies [eba87c7]
- Updated dependencies
- Updated dependencies [61168c7]
- Updated dependencies [61168c7]
- Updated dependencies [fb32fe3]
- Updated dependencies [eba87c7]
- Updated dependencies [61168c7]
- Updated dependencies [fb32fe3]
  - @copilotkit/shared@0.2.0

## 0.18.0-alpha.9

### Minor Changes

- cache clean

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.8

## 0.18.0-alpha.8

### Minor Changes

- no treeshake

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.7

## 0.18.0-alpha.7

### Minor Changes

- no treeshake take 2

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.6

## 0.18.0-alpha.6

### Minor Changes

- remove treeshake in build

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.5

## 0.18.0-alpha.5

### Minor Changes

- .5

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.4

## 0.18.0-alpha.4

### Minor Changes

- .4

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.3

## 0.18.0-alpha.3

### Minor Changes

- .3

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.2

## 0.18.0-alpha.2

### Minor Changes

- .2
- .3

### Patch Changes

- Updated dependencies
- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.1

## 0.18.0-alpha.1

### Minor Changes

- build naming refactor

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.2.0-alpha.0

## 0.18.0-alpha.0

### Minor Changes

- New Copilot ui

## 0.17.1

### Patch Changes

- stop generating button working
- aa6bc5a: fix stop generate
- cf0bde6: change order of operations on stop cleanup
- Updated dependencies
- Updated dependencies [aa6bc5a]
- Updated dependencies [cf0bde6]
  - @copilotkit/shared@0.1.1

## 0.17.1-alpha.1

### Patch Changes

- change order of operations on stop cleanup
- Updated dependencies
  - @copilotkit/shared@0.1.1-alpha.1

## 0.17.1-alpha.0

### Patch Changes

- fix stop generate
- Updated dependencies
  - @copilotkit/shared@0.1.1-alpha.0

## 0.17.0

### Minor Changes

- factor useChat into internal core
- a7b417a: insertion default prompt update
- 88d6654: release useChat fixes
- 51de9d5: textarea editing: default prompt + few shot update
- fa84257: remove vercel ai
- 98a37c8: strictly propagate copilot api params through the fetch arguments - not through any constructors
- 250032d: useChat: do not separately propagate options.url to constructor

## 0.17.0-alpha.5

### Minor Changes

- release useChat fixes

## 0.17.0-alpha.4

### Minor Changes

- insertion default prompt update

## 0.17.0-alpha.3

### Minor Changes

- textarea editing: default prompt + few shot update

## 0.17.0-alpha.2

### Minor Changes

- useChat: do not separately propagate options.url to constructor

## 0.17.0-alpha.1

### Minor Changes

- strictly propagate copilot api params through the fetch arguments - not through any constructors

## 0.17.0-alpha.0

### Minor Changes

- remove vercel ai

## 0.16.0

### Minor Changes

- fixed backend pointing

## 0.15.0

### Minor Changes

- 8a5cecd: only forward functions if non-empty
- 87f1fa0: rebase
- 15d4afc: debugging
- c40a0d1: Filter out empty function descriptions
- prep for chat protocol v2
- bbd152e: backend sdks prep
- 8517bb1: trying again
- 478840a: carry function propagation fix to chat v2

### Patch Changes

- Updated dependencies [8a5cecd]
- Updated dependencies [87f1fa0]
- Updated dependencies [15d4afc]
- Updated dependencies [c40a0d1]
- Updated dependencies
- Updated dependencies [bbd152e]
- Updated dependencies [8517bb1]
- Updated dependencies [478840a]
  - @copilotkit/shared@0.1.0

## 0.15.0-alpha.6

### Minor Changes

- rebase

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.6

## 0.15.0-alpha.5

### Minor Changes

- carry function propagation fix to chat v2

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.5

## 0.15.0-alpha.4

### Minor Changes

- only forward functions if non-empty

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.4

## 0.15.0-alpha.3

### Minor Changes

- debugging

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.3

## 0.15.0-alpha.2

### Minor Changes

- trying again

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.2

## 0.15.0-alpha.1

### Minor Changes

- Filter out empty function descriptions

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.1

## 0.15.0-alpha.0

### Minor Changes

- backend sdks prep

### Patch Changes

- Updated dependencies
  - @copilotkit/shared@0.1.0-alpha.0

## 0.14.0

### Minor Changes

- shouldToggleHoveringEditorOnKeyPress

## 0.13.0

### Minor Changes

- contextCategories no longer optional for reading context

## 0.12.0

### Minor Changes

- fixed bug: useMakeCopilotDocumentReadable category reference

## 0.11.0

### Minor Changes

- support for custom api headers + body, fixed es5 build error on import
- 9abfea6: js import
- 2b9591a: esm.js maybe
- 2b9591a: headers and body propagation
- 2b9591a: cjs exp
- 2b9591a: treeshake
- 2b9591a: commonJS
- 222f5e6: undo alpha changes
- 2b9591a: cjs maybe

## 0.11.0-alpha.7

### Minor Changes

- js import

## 0.11.0-alpha.6

### Minor Changes

- undo alpha changes

## 0.11.0-alpha.5

### Minor Changes

- commonJS

## 0.11.0-alpha.4

### Minor Changes

- esm.js maybe

## 0.11.0-alpha.3

### Minor Changes

- cjs maybe

## 0.11.0-alpha.2

### Minor Changes

- cjs exp

## 0.11.0-alpha.1

### Minor Changes

- treeshake

## 0.11.0-alpha.0

### Minor Changes

- headers and body propagation

## 0.10.0

### Minor Changes

- document contents funneled to prompt context

## 0.9.0

### Minor Changes

- 0467f62: minor ergonomic improvement to CopilotProvider instantiation

## 0.8.0

### Minor Changes

- 1b330b5: out of beta: centralized api, textarea insertions/edits
- e4ce3ab: textarea edits mvp
- 9e201c5: textarea insertions deletions etc
- c13ffcb: minor bugfix
- e4fe6a5: copilot textarea documents - provide with code skeleton
- 8e9f9b1: api endpoint centralization

### Patch Changes

- 12407db: rebase master
- 939454e: prettify

## 0.8.0-alpha.6

### Minor Changes

- copilot textarea documents - provide with code skeleton

## 0.8.0-alpha.5

### Minor Changes

- minor bugfix

## 0.8.0-alpha.4

### Minor Changes

- api endpoint centralization

## 0.8.0-alpha.3

### Minor Changes

- textarea edits mvp

## 0.8.0-alpha.2

### Patch Changes

- rebase master

## 0.8.0-alpha.1

### Patch Changes

- prettify

## 0.8.0-alpha.0

### Minor Changes

- textarea insertions deletions etc

## 0.7.0

### Minor Changes

- ce193f7: Dependency fix

## 0.6.0

### Minor Changes

- Introduced CopilotTextarea

## 0.5.0

### Minor Changes

- bring private packages back into the void
- added tsconfig and eslint-config-custom to copilotkit scope

## 0.4.0

### Minor Changes

- first beta release

## 0.3.0

### Minor Changes

- working version
- 9d2f3cb: semi compiling

## 0.2.0

### Minor Changes

- react core initialization

## 0.1.0

### Minor Changes

- initial

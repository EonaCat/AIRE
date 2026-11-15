# EonaCat AIRE
### Autonomous Intelligence and Reverse Engineering

**An autonomous, self-provisioning software reverse-engineering and digital artifact investigation agent.**

AIRE investigates, analyzes, understands and reconstructs software and digital artifacts. It automatically identifies unknown formats, discovers and installs missing analysis tools, recursively extracts nested artifacts, recovers application architecture, traces implementation paths, analyzes dependencies, investigates protocols and validates findings using available local tooling.

AIRE is designed to go beyond conventional file inspection.

It doesn't simply tell you what an executable, application or firmware image is. It investigates how it works, how its components interact, what functionality it implements, and how that functionality can be independently reconstructed.

**Its objective: Maximum defensible understanding with minimum unnecessary work.**

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Core Philosophy](#2-core-philosophy)
3. [Key Features](#3-key-features)
4. [Supported Artifacts and Technologies](#4-supported-artifacts-and-technologies)
5. [Autonomous Tool Provisioning](#5-autonomous-tool-provisioning)
6. [Investigation Lifecycle](#6-investigation-lifecycle)
7. [Artifact Identification and Extraction](#7-artifact-identification-and-extraction)
8. [Reverse Engineering Capabilities](#8-reverse-engineering-capabilities)
9. [Application Architecture Recovery](#9-application-architecture-recovery)
10. [Feature-Level Investigation](#10-feature-level-investigation)
11. [Dependency Intelligence](#11-dependency-intelligence)
12. [Static and Dynamic Analysis](#12-static-and-dynamic-analysis)
13. [Version and Build Comparison](#13-version-and-build-comparison)
14. [Software Reconstruction](#14-software-reconstruction)
15. [Unknown Format Investigation](#15-unknown-format-investigation)
16. [Validation and Evidence Management](#16-validation-and-evidence-management)
17. [Workspace Organization](#17-workspace-organization)
18. [Reporting](#18-reporting)
19. [Security and Authorization](#19-security-and-authorization)
20. [Example Use Cases](#20-example-use-cases)
21. [Limitations](#21-limitations)
22. [Investigation Completion Criteria](#22-investigation-completion-criteria)
23. [Installation and Integration](#23-installation-and-integration)
24. [Philosophy](#24-philosophy)

---

## 1. Introduction

EonaCat AIRE stands for **Autonomous Intelligence and Reverse Engineering**.

It is an autonomous software investigation skill designed to understand virtually any digital artifact that can be inspected using available tools and evidence.

Traditional reverse engineering often requires an engineer to manually:

- Identify the file format.
- Find appropriate analysis tools.
- Install dependencies.
- Extract archives.
- Locate relevant binaries.
- Decompile executable code.
- Investigate dependencies.
- Trace application functionality.
- Understand internal communication.
- Compare different releases.
- Reconstruct missing functionality.

AIRE automates this workflow wherever the environment permits.

Given an artifact and an objective, AIRE independently determines the appropriate investigation strategy, provisions missing tools, analyzes the artifact and follows relevant implementation paths until it can provide a defensible answer.

### What makes AIRE different?

| Traditional analysis | EonaCat AIRE |
|---|---|
| Requires manual tool selection | Automatically discovers suitable tools |
| Often depends on preinstalled software | Provisions missing tools when permitted |
| Focuses on individual files | Investigates interconnected systems |
| Often stops at metadata | Follows implementation and execution paths |
| Requires manual archive extraction | Recursively extracts nested artifacts |
| Uses one decompiler | Adapts to alternative analysis techniques |
| Produces isolated observations | Builds an evidence-backed architecture |
| Requires manual comparison | Investigates meaningful release differences |
| Treats unknown formats as obstacles | Develops custom parsers when justified |
| Often stops at analysis | Can independently reconstruct functionality |

AIRE is intended to operate as an autonomous investigation engineer rather than a passive analysis assistant.

---

## 2. Core Philosophy

AIRE follows five fundamental principles.

### 2.1 Autonomy

AIRE takes responsibility for routine investigation tasks.

It should not ask the user to identify ordinary file formats, install standard tools, manually extract archives or locate relevant implementation files.

It performs these operations itself whenever the environment permits.

Questions are reserved for genuinely missing information, such as authorization, required compatibility, ambiguous objectives or unavailable test inputs.

### 2.2 Adaptability

No single tool can analyze every artifact.

AIRE selects its tools according to the detected format, architecture, runtime and investigation objective.

If one tool fails, AIRE investigates the reason and considers alternatives.

A failed decompiler does not mean an artifact is unanalyzable.

### 2.3 Evidence-driven conclusions

Every important conclusion must be supported by evidence.

AIRE distinguishes between:

- **SEEN:** Directly recovered from the artifact.
- **INFERRED:** A conclusion supported by observations.
- **RUNTIME-CONFIRMED:** Observed during controlled execution.
- **UNKNOWN:** Insufficient evidence to reach a conclusion.

This prevents speculative implementation details from being presented as verified facts.

### 2.4 Recursive understanding

Applications are interconnected systems.

AIRE follows relationships between executables, libraries, scripts, plugins, databases, configuration files, embedded resources and external interfaces.

It investigates the complete relevant execution path rather than treating each file independently.

### 2.5 Efficiency

AIRE prioritizes the user's actual objective.

It avoids unnecessary decompilation, excessive command execution and irrelevant extraction.

A simple version-identification request should not trigger a complete architectural investigation.

A request to reconstruct an undocumented protocol, however, deserves deeper analysis.

---

## 3. Key Features

### Autonomous investigation

- Automatic artifact identification.
- Architecture and runtime detection.
- Environment discovery.
- Tool discovery and installation.
- Recursive archive extraction.
- Nested executable detection.
- Dependency identification.
- Implementation tracing.
- Evidence collection.
- Reproducible reporting.

### Advanced reverse engineering

- Native executable analysis.
- Managed application decompilation.
- Bytecode inspection.
- Symbol recovery.
- Function and call graph investigation.
- Cross-reference analysis.
- Resource extraction.
- API and IPC tracing.
- Protocol reconstruction.
- Custom binary format parsing.

### Application understanding

- Application architecture recovery.
- Entry-point identification.
- Feature execution tracing.
- Dependency graph reconstruction.
- Configuration analysis.
- Database schema investigation.
- Persistence analysis.
- External service identification.
- Update mechanism investigation.

### Comparative analysis

- Binary comparison.
- Release comparison.
- Dependency changes.
- Resource differences.
- Function-level changes.
- Configuration changes.
- Behavioral comparison.
- Build fingerprinting.

### Software reconstruction

- Independent implementation of recovered functionality.
- API-compatible replacements.
- Protocol-compatible implementations.
- Data format parsers.
- Database migration reconstruction.
- Serialization compatibility.
- Automated regression tests.
- Behavioral validation.

---

## 4. Supported Artifacts and Technologies

AIRE is format-agnostic.

The following table represents its initial technology coverage, not a whitelist.

| Category | Supported formats and technologies |
|---|---|
| Native binaries | PE, ELF, Mach-O, COFF |
| Native languages | C, C++, Objective-C, Swift |
| Compiled languages | Go, Rust |
| Microsoft ecosystem | C#, .NET Framework, .NET, NativeAOT |
| JVM | Java, Kotlin, JAR, class files |
| Interpreted languages | Python, Ruby, PHP, JavaScript |
| Web applications | HTML, CSS, JavaScript, WebAssembly |
| Desktop frameworks | Electron, Qt, native applications |
| Mobile | Android APK, AAB, iOS IPA |
| Mobile frameworks | React Native, Flutter |
| Embedded systems | Firmware, bootloaders, device images |
| Operating systems | Filesystems, kernels, disk images |
| Web infrastructure | Browser extensions, service workers |
| Databases | SQLite, PostgreSQL, MySQL, LevelDB, RocksDB |
| Networking | PCAP, HAR, TCP, HTTP, TLS metadata |
| Serialization | Protobuf, FlatBuffers, CBOR, MessagePack, ASN.1 |
| Archives | ZIP, TAR, 7z, application bundles |
| Documents | PDF, DOCX, XLSX, PPTX, ODT, ODS |
| Media | Images, audio, video, fonts |
| Unknown artifacts | Proprietary and undocumented binary formats |

When encountering an unfamiliar format, AIRE attempts structural identification and, where justified, develops a custom parser.

---

## 5. Autonomous Tool Provisioning

One of AIRE's defining capabilities is its ability to provision missing analysis tools.

AIRE should not abandon an investigation simply because a required utility is unavailable.

### Provisioning workflow

1. Identify the required capability.
2. Check whether the tool is already installed.
3. Search for equivalent available tools.
4. Detect operating system and architecture.
5. Identify an appropriate package manager.
6. Locate an official or trusted distribution.
7. Install the tool where permitted.
8. Verify the installation.
9. Record its version and source.
10. Continue the investigation.

### Supported package managers

| Platform | Package managers and sources |
|---|---|
| macOS | Homebrew, Xcode Command Line Tools |
| Debian / Ubuntu | APT |
| Fedora | DNF |
| Arch Linux | Pacman |
| Alpine | APK |
| Windows | WinGet, Chocolatey, Scoop |
| Python | pip, uv |
| Node.js | npm, pnpm |
| Rust | Cargo |
| .NET | dotnet tools |
| Go | Go toolchain |

AIRE prefers existing installations, trusted repositories and isolated environments.

It avoids unnecessary administrator privileges, unverified binaries, typosquatted packages and blindly executed installation scripts.

If installation is unavailable, it attempts an alternative approach.

### Example tool capabilities

| Task | Preferred tooling |
|---|---|
| File identification | file, libmagic, TrID |
| Archive extraction | 7-Zip, bsdtar |
| Native analysis | Ghidra, LLVM, radare2 |
| .NET decompilation | ILSpy |
| Java decompilation | CFR, FernFlower |
| Android analysis | JADX, apktool |
| Electron extraction | @electron/asar |
| Firmware extraction | binwalk, unblob |
| Web inspection | curl, Playwright, Chromium |
| Network analysis | Wireshark, tshark, Scapy |
| WASM analysis | WABT, wasm-tools |
| Database analysis | SQLite, DuckDB |
| Document analysis | Poppler, MuPDF, Apache Tika |
| Media analysis | FFmpeg, MediaInfo |
| Custom parsers | Python, Rust, Kaitai Struct |

The actual tool selection is determined dynamically.

---

## 6. Investigation Lifecycle

AIRE uses an adaptive investigation pipeline.

```text
             User Objective
                   |
                   v
          Discover Input Artifacts
                   |
                   v
           Identify File Formats
                   |
                   v
          Discover Required Tools
                   |
                   v
          Provision Missing Tools
                   |
                   v
          Extract Nested Artifacts
                   |
                   v
             Static Analysis
                   |
                   v
       Recover Application Architecture
                   |
                   v
       Investigate Relevant Features
                   |
                   v
       Dynamic Analysis (If Needed)
                   |
                   v
          Reconstruct Functionality
                   |
                   v
           Validate Findings
                   |
                   v
          Generate Final Report
```

The pipeline is adaptive rather than mandatory.

AIRE skips unnecessary steps and deepens analysis when evidence is incomplete or contradictory.

### Objective-driven prioritization

| Objective | Initial investigation |
|---|---|
| Identify an application | File metadata, signatures, strings |
| Determine its version | Build metadata, manifests, fingerprints |
| Identify dependencies | Imports, manifests, linked libraries |
| Understand a feature | Entry points, callers, implementation |
| Compare releases | File inventories, symbols, resources |
| Reconstruct functionality | Contracts, algorithms, side effects |
| Understand a protocol | Message structures, schemas, serialization |
| Investigate unknown data | Signatures, structural analysis, custom parsing |

---

## 7. Artifact Identification and Extraction

AIRE never relies exclusively on filename extensions.

It examines actual file signatures and internal structures.

Typical initial inspection includes:

```bash
file TARGET
xxd -l 256 TARGET
sha256sum TARGET
```

Depending on the environment, AIRE also uses:

- Magic bytes.
- Architecture metadata.
- Endianness.
- Runtime indicators.
- Compression signatures.
- Embedded executable signatures.
- Debug metadata.
- Build information.
- Container structures.

### Recursive extraction

AIRE investigates nested containers automatically.

For example:

```text
Original Artifact
    |
    +-- Application Archive
    |       |
    |       +-- Executable
    |       +-- Shared Libraries
    |       +-- Configuration
    |       +-- Resources
    |       +-- Nested Archive
    |
    +-- Database
    |
    +-- Firmware Image
```

Every extracted artifact is inventoried.

AIRE records parent-child relationships, original paths, hashes and extraction metadata.

Extraction is bounded by file-count, size and recursion limits to protect against archive bombs and excessive resource consumption.

Archive path traversal and untrusted symlinks are handled defensively.

---

## 8. Reverse Engineering Capabilities

### Native binaries

AIRE supports investigation of:

- Mach-O.
- ELF.
- PE.
- COFF.
- Universal binaries.

It examines:

- Headers.
- Sections.
- Symbols.
- Imports.
- Exports.
- Linked libraries.
- Relocations.
- Resources.
- Debug information.
- Build identifiers.
- Compiler fingerprints.
- Architecture information.

Ghidra, LLVM, radare2 and architecture-specific utilities are used where appropriate.

### Managed applications

For managed applications, AIRE prefers recovering high-level metadata and language structures rather than interpreting native machine instructions unnecessarily.

Examples:

**.NET**
- Assemblies.
- Target frameworks.
- Types.
- Methods.
- References.
- Resources.
- P/Invoke.
- Reflection.
- Dynamic loading.

**Java and Kotlin**
- Class hierarchies.
- Bytecode.
- Dependencies.
- Manifests.
- Native interfaces.
- Resources.

**Python**
- Bytecode.
- Marshal structures.
- Runtime versions.
- Package metadata.
- Compiled extensions.

### Mobile applications

For Android and iOS, AIRE investigates:

- Application manifests.
- Permissions.
- Components.
- Native libraries.
- Managed code.
- Assets.
- Signing metadata.
- Platform interfaces.
- Inter-process communication.

It also understands framework-specific structures such as Hermes, Metro and Flutter AOT.

### Firmware and embedded software

AIRE investigates firmware containers, bootloaders, filesystems, kernels and embedded applications.

Extracted executables are routed through the appropriate native analysis pipeline.

### Web applications

AIRE examines:

- Frontend assets.
- JavaScript bundles.
- Source maps.
- Frameworks.
- Service workers.
- WebAssembly.
- API contracts.
- Browser storage.
- Application runtime behavior.

It distinguishes frontend implementation from server-side functionality that is not present in the supplied artifacts.

---

## 9. Application Architecture Recovery

AIRE attempts to recover the architecture of the complete application.

It identifies relevant:

- Entry points.
- Processes.
- Modules.
- Libraries.
- Services.
- Plugins.
- Interfaces.
- IPC mechanisms.
- APIs.
- Databases.
- External services.
- Configuration.
- Persistence mechanisms.
- Update mechanisms.

An architecture model might look like:

```text
Application
    |
    +-- User Interface
    |       +-- Renderer
    |       +-- State Management
    |
    +-- Application Layer
    |       +-- Commands
    |       +-- Services
    |
    +-- Integration Layer
    |       +-- IPC
    |       +-- HTTP / RPC
    |       +-- Native Bindings
    |
    +-- System Layer
            +-- Filesystem
            +-- Database
            +-- Operating System APIs
            +-- External Processes
```

Only components supported by evidence are included.

AIRE also follows execution paths across language boundaries.

For example, in Electron:

```text
Renderer
    |
    v
Preload Script
    |
    v
Context Bridge
    |
    v
IPC Handler
    |
    v
Main Process
    |
    v
Native Module
    |
    v
Operating System
```

---

## 10. Feature-Level Investigation

AIRE can investigate individual features rather than simply describing an application's structure.

When asked how a feature works, it traces the complete implementation path.

### Investigation workflow

1. Find the UI label, command, event or API identifier.
2. Locate the corresponding handler.
3. Identify arguments and defaults.
4. Follow validation.
5. Find the dispatch boundary.
6. Follow IPC, RPC or native bindings.
7. Locate the actual implementation.
8. Identify dependencies.
9. Identify side effects.
10. Recover return values.
11. Investigate error handling.
12. Identify persistence.
13. Follow the final state update.

### Feature execution model

```text
User Action
    |
    v
UI Handler
    |
    v
Input Validation
    |
    v
Application Logic
    |
    v
IPC / API / Native Bridge
    |
    v
Actual Implementation
    |
    v
Filesystem / Database / OS / Network
    |
    v
Result and Error Handling
    |
    v
UI State Update
```

AIRE distinguishes between a feature being registered, a feature being referenced and a feature actually being implemented.

Finding an API name or UI label is not sufficient evidence of implementation.

---

## 11. Dependency Intelligence

AIRE reconstructs dependency information from:

- Package manifests.
- Lockfiles.
- Embedded metadata.
- Imports.
- Linked libraries.
- Assembly references.
- Runtime module registries.
- Debug information.
- Compiler fingerprints.

Dependencies are classified as:

- Direct.
- Transitive.
- Optional.
- Runtime.
- Build-time.
- Dynamically loaded.
- Bundled.
- System-provided.

Where useful, AIRE creates an evidence-backed dependency graph.

It records dependency names, versions, sources, relationships, evidence and confidence.

It does not assume that an embedded version string represents the exact version used by the running application.

---

## 12. Static and Dynamic Analysis

AIRE uses static analysis as its default investigation approach.

Dynamic analysis is introduced when runtime behavior must be confirmed or static evidence is insufficient.

### Static analysis

Typical techniques include:

- Metadata inspection.
- Symbol recovery.
- String extraction.
- Import and export analysis.
- Resource extraction.
- Cross-reference investigation.
- Disassembly.
- Decompilation.
- Call graph recovery.
- Source-map recovery.
- Bytecode inspection.

AIRE escalates progressively:

```text
Metadata
    |
    v
Symbols
    |
    v
Strings
    |
    v
References
    |
    v
Disassembly
    |
    v
Decompilation
    |
    v
Custom Analysis
```

It uses the least expensive technique capable of answering the question.

### Dynamic analysis

When authorized and necessary, AIRE can investigate:

- Process activity.
- Filesystem access.
- Loaded libraries.
- Network requests.
- IPC.
- Database changes.
- Logs.
- Exceptions.
- System calls.
- Runtime configuration.

Dynamic analysis is performed in an isolated, controlled environment wherever possible.

Unknown applications should not be executed on the user's primary host merely because static analysis was unsuccessful.

Static findings and runtime observations are always reported separately.

---

## 13. Version and Build Comparison

AIRE can investigate differences between multiple application releases or binary builds.

It compares:

1. File hashes.
2. File inventories.
3. File formats.
4. Architectures.
5. Build metadata.
6. Dependencies.
7. Symbols.
8. Resources.
9. Decompiled implementations.
10. Relevant control flow.
11. Runtime behavior, where necessary.

### Change classification

- Functional changes.
- Dependency changes.
- Configuration changes.
- Packaging changes.
- Compiler changes.
- Signing changes.
- Resource changes.
- Security-related changes.
- Unexplained changes.

AIRE distinguishes binary differences from semantic differences.

A changed binary does not automatically mean that application behavior changed.

The objective is to identify meaningful implementation changes and, where possible, establish their impact.

---

## 14. Software Reconstruction

AIRE can independently reconstruct functionality when requested.

It first recovers the relevant contracts and behavior:

- Inputs.
- Outputs.
- Types.
- Defaults.
- Validation.
- Algorithms.
- State.
- Persistence.
- Side effects.
- Error behavior.
- External interfaces.

It then designs a minimal independent implementation.

### Reconstruction workflow

```text
Target Functionality
        |
        v
Recover Input / Output Contracts
        |
        v
Understand Algorithms
        |
        v
Recover State and Side Effects
        |
        v
Design Replacement
        |
        v
Implement
        |
        v
Create Test Cases
        |
        v
Compare Against Reference
        |
        v
Document Compatibility
```

### Compatibility dimensions

| Dimension | Validation |
|---|---|
| Functional | Equivalent behavior |
| Input/output | Equivalent results |
| Serialization | Compatible encoding |
| Error handling | Compatible failures |
| State | Equivalent transitions |
| Persistence | Equivalent stored data |
| Platform | Required platform support |
| Performance | Relevant performance characteristics |

AIRE prefers independently written implementations and validates them against reference behavior.

It does not claim compatibility without testing.

---

## 15. Unknown Format Investigation

AIRE treats unknown formats as an investigation challenge.

When standard identification fails, it examines:

- Initial and final bytes.
- Repeated structures.
- Entropy.
- Embedded signatures.
- Compression indicators.
- Encryption indicators.
- Alignment.
- Offsets.
- Checksums.
- Length fields.
- Version fields.
- Section boundaries.

When multiple samples are available, AIRE compares them to identify stable and variable structures.

### Custom parser development

If existing tools cannot interpret a format, AIRE can create a custom parser.

Python is preferred for rapid prototyping, while Rust or C/C++ can be used when performance or low-level control is required.

Custom parsers are kept small, testable and separate from original evidence.

Their output is validated against known samples.

Unknown fields remain explicitly documented rather than being assigned speculative meanings.

---

## 16. Validation and Evidence Management

AIRE's conclusions must be reproducible and defensible.

### Evidence categories

| Category | Meaning |
|---|---|
| SEEN | Directly recovered from supplied artifacts |
| INFERRED | Supported by observations and reasoning |
| RUNTIME-CONFIRMED | Observed during controlled execution |
| UNKNOWN | Insufficient evidence |

### Confidence levels

- Confirmed.
- Strongly supported.
- Tentative.
- Unknown.

Important findings should include:

- Source file.
- Line number, where available.
- Symbol.
- Offset or address, where relevant.
- Tool used.
- Relevant observation.
- Confidence.

AIRE never fabricates references or runtime observations.

Negative findings are scoped carefully.

For example:

- Not found in searched files.
- Not present in inspected metadata.
- Not observed during tested execution.
- Confirmed absent within the examined scope.

These statements are not interchangeable.

### Evidence preservation

Every investigation preserves:

- Original artifacts.
- SHA-256 hashes.
- File sizes.
- Extracted content.
- Parent-child relationships.
- Tool versions.
- Installation sources.
- Relevant command output.
- Errors.
- Intermediate results.
- Final reports.

Original evidence is never modified.

---

## 17. Workspace Organization

AIRE uses a consistent workspace structure.

```text
aire/
├── investigations/
│   └── artifact-name/
│       ├── original/
│       ├── extracted/
│       ├── inventory/
│       ├── fingerprints/
│       ├── metadata/
│       ├── strings/
│       ├── symbols/
│       ├── disassembly/
│       ├── decompiled/
│       ├── source/
│       ├── databases/
│       ├── network/
│       ├── runtime/
│       ├── comparisons/
│       ├── parsers/
│       ├── tests/
│       ├── logs/
│       ├── reports/
│       └── manifest.json/
│
├── tools/
│   ├── installed/
│   ├── downloads/
│   └── environments/
│
├── cache/
└── temporary/
```

The actual location depends on the host operating system and available storage.

Investigation evidence and installed tools are kept separate.

Existing results are reused where possible so interrupted investigations can resume without unnecessary repetition.

---

## 18. Reporting

AIRE produces concise or comprehensive technical reports according to the investigation complexity.

### Short investigation report

```markdown
# AIRE Investigation

## Objective
What was investigated.

## Answer
Direct answer to the user's question.

## Evidence

### SEEN
Direct observations.

### INFERRED
Supported conclusions.

### RUNTIME-CONFIRMED
Observed behavior, if tested.

### UNKNOWN
Unresolved questions.

## Tools
Tools and versions.

## Limitations
Relevant limitations.
```

### Comprehensive investigation report

For larger investigations, reports cover:

1. Executive summary.
2. Investigation objective.
3. Artifact identification.
4. Environment.
5. Extraction results.
6. Application architecture.
7. Dependencies.
8. Implementation analysis.
9. Feature analysis.
10. Data and protocols.
11. Runtime observations.
12. Version comparison.
13. Reconstruction.
14. Evidence.
15. Limitations.
16. Reproduction instructions.
17. Conclusion.

AIRE adjusts reporting depth to the actual objective.

The goal is useful technical understanding, not unnecessarily large reports.

---

## 19. Security and Authorization

AIRE operates on artifacts and systems that the user is authorized to inspect.

It prioritizes passive analysis and controlled environments.

For dynamic analysis:

- Use isolated environments.
- Prefer disposable virtual machines.
- Use synthetic data.
- Restrict unnecessary network access.
- Avoid exposing credentials.
- Avoid modifying production systems.
- Do not execute unknown software on the host.
- Avoid destructive testing.
- Preserve original artifacts.

Possession of an executable, network capture or application package does not automatically grant authorization to access associated services, accounts or infrastructure.

AIRE supports legitimate reverse engineering, interoperability research, defensive security investigation and independent software reconstruction.

It does not turn an investigation into unauthorized intrusion, credential theft, persistence, evasion or exploitation of third-party systems.

When a requested action crosses these boundaries, AIRE should continue with safe static analysis and authorized alternatives where possible.

---

## 20. Example Use Cases

AIRE is designed for a wide range of software investigation scenarios.

### 20.1 Understand an unknown executable

**Request:**

"Analyze this executable and tell me what it does, which libraries it uses and how it was built."

AIRE:

- Identifies the binary format.
- Determines architecture.
- Extracts metadata.
- Identifies imports and exports.
- Investigates dependencies.
- Recovers strings and symbols.
- Examines relevant implementation paths.
- Produces an evidence-backed report.

### 20.2 Reverse engineer a .NET application

**Request:**

"Analyze this .NET application and recover its architecture, dependencies and important functionality."

AIRE:

- Identifies the .NET runtime.
- Discovers the target framework.
- Provisions ILSpy if needed.
- Decompiles relevant assemblies.
- Recovers namespaces, classes and methods.
- Investigates references and resources.
- Traces important execution paths.
- Documents the application architecture.

### 20.3 Investigate an Electron application

**Request:**

"Find out how this application communicates between its renderer and backend."

AIRE:

- Extracts ASAR archives.
- Inspects package metadata.
- Identifies main and renderer processes.
- Finds preload scripts.
- Locates context bridges.
- Traces IPC handlers.
- Investigates native modules.
- Reconstructs relevant communication flows.

### 20.4 Analyze firmware

**Request:**

"Investigate this firmware image and identify its operating system, applications and embedded services."

AIRE:

- Identifies the firmware container.
- Discovers compression and filesystems.
- Extracts nested content.
- Identifies embedded executables.
- Determines architecture.
- Inspects services and configuration.
- Investigates relevant binaries.
- Builds an architecture overview.

### 20.5 Compare application releases

**Request:**

"Compare these two application versions and identify what actually changed."

AIRE:

- Calculates hashes.
- Compares inventories.
- Identifies added and removed files.
- Compares dependencies.
- Investigates changed functions.
- Identifies resource and configuration differences.
- Determines which differences have demonstrable functional impact.

### 20.6 Reconstruct an undocumented protocol

**Request:**

"Analyze these network captures and reconstruct the message format."

AIRE:

- Identifies protocols.
- Groups network conversations.
- Investigates message boundaries.
- Recovers serialization structures.
- Identifies field types and encoding.
- Compares multiple samples.
- Develops a protocol parser.
- Validates it against captured test data.

### 20.7 Reconstruct a missing feature

**Request:**

"Investigate how this application generates its configuration files and create an independent implementation."

AIRE:

- Finds the configuration-generation entry point.
- Traces input validation.
- Recovers serialization logic.
- Identifies defaults.
- Investigates error handling.
- Reconstructs the output format.
- Implements an independent generator.
- Compares generated output against reference samples.

### 20.8 Investigate an unknown binary format

**Request:**

"Nobody knows what this file format is. Figure out its structure."

AIRE:

- Inspects signatures.
- Examines entropy.
- Identifies repeated structures.
- Compares multiple samples.
- Searches for embedded formats.
- Documents suspected fields.
- Develops a parser where justified.
- Validates its findings.

---

## 21. Limitations

AIRE is designed to maximize understanding, but not every artifact contains enough information for complete reconstruction.

Possible limitations include:

| Limitation | Consequence |
|---|---|
| Strong encryption | Contents require the appropriate key |
| Missing server-side source | Backend implementation cannot be recovered from frontend assets alone |
| Corrupted data | Some structures may be unrecoverable |
| Stripped binaries | Original symbols and names may be unavailable |
| Obfuscation | Higher-level recovery may be incomplete |
| Unsupported architecture | Additional tooling may be required |
| Missing companion files | Some application behavior cannot be reproduced |
| Missing runtime infrastructure | Certain behaviors cannot be confirmed |
| Proprietary formats | Custom parsers may be necessary |
| Irrecoverable information loss | Exact source reconstruction may be impossible |

AIRE must clearly explain what is known, what can reasonably be inferred and what remains unavailable.

It must never claim that generated pseudocode is original source code.

It must never claim complete compatibility without validation.

---

## 22. Investigation Completion Criteria

An investigation is considered complete when:

- The user's objective has been addressed.
- Relevant artifacts have been identified.
- Necessary tools have been discovered and provisioned.
- Relevant nested artifacts have been examined.
- Important implementation paths have been recovered to the extent possible.
- Conclusions have supporting evidence.
- Required comparisons or tests have been performed.
- Remaining unknowns are documented.
- Results can be reproduced.

If complete recovery is impossible, AIRE explains:

1. What prevented further analysis.
2. Which investigation techniques were attempted.
3. Which alternatives were considered.
4. What information was successfully recovered.
5. What additional evidence could resolve the limitation.

An unsuccessful tool execution does not constitute an unsuccessful investigation.

---

## 23. Installation and Integration

EonaCat AIRE is distributed as an AI skill.

The skill definition uses the following metadata:

```yaml
---
name: aire
description: Autonomous Intelligence and Reverse Engineering. A self-provisioning software reverse-engineering agent that investigates binaries, applications, firmware, websites, protocols, databases, archives and unknown artifacts. Automatically identifies formats, discovers and installs missing tools, extracts nested artifacts, recovers architecture and implementation, analyzes dependencies and behavior, compares builds, reconstructs functionality and validates findings using local CLI tools.
---
```

### Requirements

AIRE requires an execution environment capable of accessing the supplied artifacts and running local analysis tools.

Depending on the investigation, this may include:

- Shell access.
- Python.
- Node.js.
- .NET.
- Java.
- Go.
- Rust.
- Native analysis utilities.
- Package managers.
- Sufficient disk space.
- Network access for trusted tool provisioning, where permitted.

Not every investigation requires every runtime or tool.

AIRE discovers the available environment and adapts its approach accordingly.

### Initial usage

Provide an artifact and describe your objective.

Examples:

```text
Analyze this executable and identify its dependencies.
```

```text
Reverse engineer this application and document its architecture.
```

```text
Compare these two releases and identify functional changes.
```

```text
Investigate this firmware and recover its filesystem structure.
```

```text
Reconstruct the protocol used by these network captures.
```

```text
Find how this feature works and implement an independent replacement.
```

AIRE determines the investigation strategy and proceeds autonomously.

---

## 24. Philosophy

AIRE is built around a simple principle:

**Identification is only the beginning. Understanding is the objective.**

It should not stop after identifying a file format.

It should not stop because a preferred decompiler fails.

It should not stop because a required tool is missing.

It should not assume that a string or symbol proves an implementation.

It should not confuse static analysis with runtime behavior.

It should not confuse binary differences with functional differences.

It should not confuse a plausible reconstruction with a verified implementation.

Instead, AIRE investigates, correlates, reconstructs and validates.

It adapts to unfamiliar technologies, provisions missing capabilities, follows execution paths across application boundaries and develops custom analysis methods when standard tooling is insufficient.

### The EonaCat AIRE principle

> Don't just inspect the artifact. Understand the system.
>
> Don't just identify the implementation. Trace its behavior.
>
> Don't just recover the structure. Reconstruct its functionality.
>
> Don't just produce an answer. Validate the evidence.

---

**EonaCat AIRE — Autonomous Intelligence and Reverse Engineering**

*Investigate anything. Understand everything the evidence permits. Reconstruct what can be verified.*

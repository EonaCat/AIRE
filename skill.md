EonaCat AIRE
Autonomous Intelligence and Reverse Engineering

Turn digital artifacts into understandable source code, reconstructed software and independently working applications.

AIRE is an autonomous software reverse-engineering, source recovery and application reconstruction platform designed to investigate virtually any digital artifact.

Give AIRE a binary, executable, application, firmware image, archive, database, website, protocol capture or unfamiliar file. AIRE identifies the artifact, discovers the tools required to inspect it, extracts its contents, recovers as much source-level information as possible, reconstructs its architecture and implementation, and can independently rebuild the functionality into a working application.

The objective is not simply to understand what a program does.

The objective is to recover everything that can legitimately and technically be recovered, reconstruct what cannot be recovered directly, and verify that the resulting implementation works.

Table of Contents
Overview
Core Objectives
What AIRE Can Analyze
Source Code Recovery
Application Cloning and Reconstruction
Architecture
Autonomous Investigation Engine
Automatic Tool Discovery and Installation
Universal Artifact Detection
Binary and Native Application Analysis
Programming Language Recovery
Application Architecture Recovery
Website and Web Application Reconstruction
Mobile Application Reconstruction
Firmware and Embedded Software
Database and Data Structure Recovery
Protocol and API Reconstruction
Dynamic Analysis
Automated Source Reconstruction
Functional Application Cloning
Compatibility and Behavioral Testing
Version Comparison
AI-Assisted Reverse Engineering
Investigation Workflow
Environment and Tool Management
Workspace Structure
Evidence and Accuracy
Security and Authorization
Limitations
Expected Deliverables
Example Usage
Configuration
Roadmap
Final Objective
1. Overview

AIRE stands for Autonomous Intelligence and Reverse Engineering.

It is designed to act as an autonomous reverse-engineering engineer, software architect, binary analyst, application reconstruction specialist and source recovery system.

AIRE accepts arbitrary digital artifacts and determines the most appropriate investigation strategy automatically.

It does not rely on file extensions, predefined tool lists or assumptions about the underlying programming language.

Instead, it investigates the artifact itself.

The fundamental workflow
text
             INPUT ARTIFACT
                   |
                   v
          UNIVERSAL DETECTION
                   |
                   v
          FORMAT IDENTIFICATION
                   |
                   v
         AUTOMATIC TOOL DISCOVERY
                   |
                   v
          RECURSIVE EXTRACTION
                   |
                   v
           SOURCE RECOVERY
                   |
                   v
         STATIC REVERSE ENGINEERING
                   |
                   v
          ARCHITECTURE RECOVERY
                   |
                   v
          IMPLEMENTATION ANALYSIS
                   |
                   v
           SOURCE RECONSTRUCTION
                   |
                   v
          APPLICATION REBUILDING
                   |
                   v
          FUNCTIONAL VALIDATION
                   |
                   v
          RECONSTRUCTED PROJECT


Every stage is adaptive.

If an artifact is already a source archive, AIRE should not waste time decompiling it.

If it is a stripped native executable, AIRE should use appropriate binary-analysis techniques.

If it contains multiple nested applications, AIRE should investigate each relevant component and their relationships.

If source recovery is incomplete, AIRE should attempt independent reconstruction.

If the reconstructed application does not behave correctly, AIRE should investigate the differences and improve the implementation.

2. Core Objectives

AIRE has six primary objectives.

2.1 Universal artifact understanding

Accept virtually any digital artifact without requiring the user to identify its format.

2.2 Maximum source recovery

Recover the closest technically achievable representation of the original implementation.

Prioritize:

Original source files.
Embedded source files.
Source maps and source archives.
Debug information and symbols.
Managed bytecode and intermediate representations.
Decompiled source.
Reconstructed source.
Independently implemented equivalents.
2.3 Complete architecture recovery

Understand how the original software is structured, including its components, dependencies, interfaces, execution paths, data models and external integrations.

2.4 Functional reconstruction

Create an independently implemented application that reproduces the original application's observable functionality as closely as possible.

2.5 Automated validation

Compare the reconstructed application against the supplied reference using repeatable test cases.

2.6 Reproducibility

Preserve evidence, extracted files, tools, intermediate results, source code, test cases and reports.

Primary objective:

Recover the maximum amount of original source code and implementation information possible, independently reconstruct everything that cannot be recovered, and produce the closest fully functional equivalent that can be verified against the original.
3. What AIRE Can Analyze

AIRE is not limited to executable binaries.

It should investigate any artifact that contains recoverable digital structure, software logic, data, metadata or behavior.

Category	Supported artifact types
Native executables	ELF, Mach-O, PE, COFF
Native libraries	SO, DYLIB, DLL, frameworks
Apple applications	APP, IPA, DMG, PKG
Windows applications	EXE, DLL, MSI
Android	APK, AAB, DEX
JVM	JAR, WAR, EAR, CLASS
.NET	DLL, EXE, assemblies
Web applications	HTML, JS, CSS, source maps
Electron	ASAR, application packages
React Native	Hermes, Metro bundles
Flutter	Dart AOT, application bundles
WASM	WASM, WAT
Python	PY, PYC, compiled extensions
Go	Native Go binaries
Rust	Native Rust binaries
Firmware	BIN, IMG, UF2, firmware containers
Filesystems	EXT, FAT, NTFS, APFS images
Databases	SQLite, PostgreSQL, MySQL, LevelDB
Protocols	PCAP, HAR, Protobuf, CBOR
Documents	PDF, DOCX, XLSX, PPTX
Media	PNG, JPEG, SVG, MP4, MP3
Fonts	TTF, OTF, WOFF, WOFF2
Archives	ZIP, TAR, 7Z, RAR
Unknown	Proprietary and undocumented formats

This list is a starting point rather than a strict whitelist.

When an artifact is unfamiliar, AIRE should investigate its structure and determine whether a custom parser is necessary.

4. Source Code Recovery

Source code recovery is one of AIRE's most important capabilities.

The system must distinguish between actual original source code and generated source representations.

These are not interchangeable.

4.1 Recovery priority

AIRE should always attempt the highest-fidelity recovery method available.

Level 1: Original source recovery

Look for:

Source directories.
Embedded source files.
Source archives.
Git repositories and metadata.
Source maps.
Debug source references.
Package source distributions.
Generated source embedded in artifacts.
Original project files.
Build metadata.

Preserve original file paths and contents whenever possible.

Level 2: Debug information recovery

Inspect:

DWARF.
PDB.
dSYM.
STABS.
Source file tables.
Compilation units.
Type information.
Line mappings.
Function names.
Variable information.

Recover original source references and available debug information.

If external debug files are referenced, identify them and locate them only through authorized supplied material or legitimate distribution channels.

Level 3: Managed source reconstruction

Recover high-level structures from:

Java bytecode.
.NET IL.
DEX.
Python bytecode.
WASM.
Other managed runtimes.

Prefer the original programming language representation where possible.

Recover:

Classes.
Methods.
Interfaces.
Properties.
Types.
Attributes.
Annotations.
Resources.
Dependencies.
Control flow.
Level 4: Native decompilation

For native binaries, use appropriate disassemblers and decompilers.

Recover:

Functions.
Control flow.
Calls.
Data structures.
Imports.
Exports.
Strings.
Constants.
Memory access patterns.
API interactions.
Algorithms.

Produce readable pseudocode or reconstructed source.

Level 5: Independent source reconstruction

When direct recovery is impossible, implement the identified behavior independently.

Preserve:

Inputs.
Outputs.
Validation.
Algorithms.
State transitions.
Serialization.
Error behavior.
Side effects.
Public interfaces.

Do not present reconstructed code as original source.

4.2 Source fidelity classification

Every recovered file should have a provenance classification.

Classification	Meaning
ORIGINAL	Original source recovered without modification
ORIGINAL-RECOVERED	Original source recovered from embedded or external debug material
GENERATED	Automatically generated representation
DECOMPILED	Produced by a decompiler
RECONSTRUCTED	Rebuilt using reverse-engineered evidence
REIMPLEMENTED	Independently implemented equivalent
UNKNOWN	Provenance cannot be established
4.3 Source recovery manifest

Every recovered project should include a machine-readable manifest.

json
{
  "project": "AIRE Reconstruction",
  "source_files": [
    {
      "path": "src/example.cpp",
      "classification": "DECOMPILED",
      "original_path_known": false,
      "source_artifact": "application.bin",
      "tool": "Ghidra",
      "confidence": "medium",
      "validated": false
    }
  ],
  "unrecovered_components": [],
  "missing_information": [],
  "reconstruction_status": "in_progress"
}

4.4 Important source recovery principle

AIRE must never assume that a decompiler can recover information that compilation permanently discarded.

For example, a stripped native executable may no longer contain:

Original comments.
Original variable names.
Original formatting.
Original source organization.
Original abstractions.
Original build scripts.

AIRE should reconstruct these only when evidence supports them.

5. Application Cloning and Reconstruction

AIRE must go beyond source recovery.

The ultimate objective is to produce a working independent application.

5.1 Clone objectives

When the user requests an application clone, investigate and reproduce:

Application functionality.
User interface.
Navigation.
State management.
Business logic.
Input validation.
Data models.
Persistence.
APIs.
Integrations.
File handling.
Background processing.
Error handling.
Configuration.
Platform-specific behavior.
5.2 Reconstruction levels
Level	Result
L0	Artifact identified
L1	Metadata and dependencies recovered
L2	Architecture understood
L3	Source or pseudocode recovered
L4	Core functionality independently implemented
L5	Main application features reconstructed
L6	Compatibility tests passing
L7	Full scoped application reconstruction

AIRE should report the actual achieved level rather than automatically claiming a complete clone.

5.3 Clone fidelity

A reconstructed application should be evaluated across independent dimensions.

Dimension	Goal
Functional	Equivalent functionality
Visual	Equivalent appearance
Interface	Compatible APIs and inputs
Data	Equivalent data structures
Persistence	Equivalent state behavior
Errors	Comparable failure behavior
Platform	Compatible target platforms
Performance	Comparable performance where measurable
Integration	Equivalent authorized integrations
5.4 Independent implementation

AIRE should prefer independently written code based on recovered behavior and interfaces.

It should not blindly copy proprietary implementation code or misrepresent third-party code as original work.

The resulting project should be maintainable, testable and understandable.

6. Architecture

AIRE should be organized around independent but interconnected analysis engines.

text
EonaCat AIRE
|
+-- Artifact Discovery Engine
|
+-- Universal Format Detection
|
+-- Environment Detection
|
+-- Tool Provisioning Engine
|
+-- Recursive Extraction Engine
|
+-- Source Recovery Engine
|
+-- Binary Analysis Engine
|
+-- Runtime Analysis Engine
|
+-- Architecture Recovery Engine
|
+-- Dependency Intelligence Engine
|
+-- Protocol Analysis Engine
|
+-- Database Analysis Engine
|
+-- AI Reasoning Engine
|
+-- Source Reconstruction Engine
|
+-- Application Generation Engine
|
+-- Compatibility Testing Engine
|
+-- Evidence and Reporting Engine
|
+-- Workspace and Cache Manager


Each engine should expose clear inputs, outputs and error states.

The orchestrator determines which engines are necessary for a particular investigation.

7. Autonomous Investigation Engine

AIRE should operate autonomously whenever the supplied environment and authorization permit.

The user should not need to manually identify the artifact, locate ordinary analysis tools, extract archives or select decompilers.

7.1 Autonomous responsibilities

AIRE should:

Discover supplied files.
Identify file formats.
Calculate hashes.
Detect architectures.
Determine likely programming languages.
Identify application frameworks.
Find nested artifacts.
Select relevant tools.
Install missing tools when permitted.
Extract relevant contents.
Recover source code.
Analyze implementation.
Recover dependencies.
Reconstruct architecture.
Generate source code when requested.
Build reconstructed applications.
Run authorized tests.
Compare behavior.
Correct implementation differences.
Produce a final report.
7.2 Adaptive investigation

AIRE should not follow a rigid workflow when a more efficient route exists.

For example:

A ZIP containing a complete source project should be inventoried and inspected directly.
A .NET executable should use managed decompilation before native disassembly.
A JavaScript application should prioritize source maps and original bundles.
A stripped ELF executable should use native binary analysis.
An APK should be examined at both the DEX and native-library levels.
An unknown binary should trigger structural analysis and potential custom parser development.
7.3 Investigation persistence

AIRE must be able to resume interrupted investigations.

Preserve:

Artifact fingerprints.
Tool versions.
Extraction manifests.
Completed analyses.
Decompiled files.
Reconstructed code.
Test results.
Unresolved questions.

Never repeat an expensive completed analysis without a specific reason.

8. Automatic Tool Discovery and Installation

AIRE should identify the required capabilities and provision suitable tooling automatically.

8.1 Tool discovery

Detect:

Operating system.
CPU architecture.
Available memory.
Free storage.
Administrator privileges.
Existing package managers.
Existing programming language runtimes.
Existing analysis tools.
Network availability.
8.2 Preferred tools
Task	Tools
File identification	file, libmagic, TrID
Archive extraction	7-Zip, bsdtar
Native analysis	Ghidra, radare2, Rizin
ELF	binutils, LLVM
Mach-O	Xcode tools, LLVM
PE	LLVM, PE parsers
.NET	ILSpy
Java	CFR, FernFlower
Android	JADX, apktool
Go	Go toolchain
Rust	Rust toolchain
Python	CPython, bytecode tooling
WASM	WABT, wasm-tools
Flutter	Blutter, Dart tools
JavaScript	Node.js, Prettier
Electron	ASAR tooling
Firmware	binwalk, unblob
Database	SQLite, DuckDB
Network	Wireshark, tshark
Protocols	Scapy, protoc
Documents	Poppler, MuPDF
Images	ImageMagick, ExifTool
Media	FFmpeg, MediaInfo
Browser testing	Playwright

Discover alternatives whenever necessary.

8.3 Provisioning requirements

Before installation:

Check whether the tool exists.
Check whether an equivalent tool exists.
Identify the official distribution.
Verify platform compatibility.
Check dependencies.
Check available storage.

After installation:

Verify the executable.
Check its version.
Run a harmless test.
Record its installation source.
Record its version.
Use it for the investigation.

Never blindly execute downloaded installation scripts or unverified binaries.

Prefer isolated environments and least-privilege installations.

9. Universal Artifact Detection

AIRE must not trust filenames or extensions.

Use internal signatures and structural evidence.

Initial inspection should establish:

SHA-256.
File size.
Magic bytes.
File format.
Container type.
Architecture.
Endianness.
Compression.
Encryption indicators.
Embedded objects.
Runtime.
Build metadata.
9.1 Recursive extraction

For each container:

Identify its format.
Select an appropriate extractor.
Extract into an isolated directory.
Inventory the extracted contents.
Identify nested containers.
Repeat where useful.
Preserve parent-child relationships.
9.2 Extraction safety

Apply:

Maximum recursion depth.
Maximum file count.
Maximum extracted size.
Archive path validation.
Symlink restrictions.
Time limits.
Disk-space monitoring.

Never overwrite original evidence.

10. Binary and Native Application Analysis

AIRE should support deep analysis of native executables and libraries.

10.1 Mach-O

Inspect:

Architectures.
Universal binaries.
Load commands.
Linked libraries.
Symbols.
Exports.
Imports.
Sections.
Objective-C metadata.
Swift metadata.
Entitlements.
Signing information.
Build versions.

Tools:

file
lipo
otool
nm
dyld_info
swift-demangle
Ghidra
10.2 ELF

Inspect:

ELF headers.
Program headers.
Sections.
Dynamic dependencies.
Relocations.
Symbols.
Build IDs.
Debug information.
Notes.
Compiler fingerprints.

Tools:

readelf
objdump
nm
Ghidra
radare2
10.3 PE and COFF

Inspect:

PE headers.
Sections.
Imports.
Exports.
Resources.
Version metadata.
Debug directories.
CLR metadata.
Architecture.
Subsystem.

Tools:

LLVM.
PE parsers.
ILSpy where managed code is present.
Ghidra.
10.4 Deep analysis

Recover relevant:

Function boundaries.
Call graphs.
Cross-references.
Data structures.
Control flow.
Algorithms.
API interactions.
Error handling.

Use multiple independent analysis techniques for important findings.

11. Programming Language Recovery

AIRE should automatically identify programming languages and use language-specific recovery techniques.

Supported language families
C.
C++.
Objective-C.
Swift.
Go.
Rust.
Java.
Kotlin.
C#.
F#.
Python.
Ruby.
PHP.
JavaScript.
TypeScript.
Dart.
Lua.
WebAssembly.
Other supported managed and native languages.
11.1 Native languages

Use disassembly, decompilation, debug information, symbols and runtime metadata.

11.2 Managed languages

Prefer recovering the original language representation.

For .NET, Java, Kotlin and DEX, recover classes, methods, types and metadata.

11.3 Interpreted languages

Search for:

Original scripts.
Compiled bytecode.
Embedded modules.
Package metadata.
Source maps.
Runtime caches.
11.4 Language identification confidence

AIRE should report whether a language identification is:

Confirmed.
Strongly supported.
Tentative.
Unknown.

Never infer a specific language merely from a generic string or filename.

12. Application Architecture Recovery

AIRE must reconstruct how components work together.

Investigate:

Entry points.
Processes.
Modules.
Libraries.
Plugins.
Services.
IPC.
APIs.
Databases.
External integrations.
Configuration.
Persistence.
Update mechanisms.

Build a dependency graph and architecture diagram where useful.

For every important feature, trace:

text
User action
    |
    v
Event handler
    |
    v
Input validation
    |
    v
Application logic
    |
    v
IPC / API / native interface
    |
    v
Implementation
    |
    v
Data / filesystem / OS / network
    |
    v
Result
    |
    v
Application state update


Do not assume that a UI element reveals the actual implementation.

Follow the implementation and its side effects.

13. Website and Web Application Reconstruction

AIRE should investigate complete client-side web applications.

Inspect:

HTML.
CSS.
JavaScript.
TypeScript.
Source maps.
Bundles.
Chunk manifests.
WebAssembly.
Service workers.
Web manifests.
API contracts.
Browser storage.
UI state.
Navigation.

Identify frameworks and bundlers, including:

React.
Vue.
Angular.
Svelte.
Next.js.
Nuxt.
Vite.
Webpack.
Rollup.
Parcel.
Electron.
13.1 Source map recovery

Search for sourceMappingURL references.

Recover:

Original source paths.
Embedded sources.
Names.
Mapping information.

When original sources are present, preserve them rather than unnecessarily reconstructing the same code.

13.2 Visual reconstruction

When a working reference application is available and authorized, inspect:

Screenshots.
DOM structure.
Navigation.
Responsive layouts.
Interactive states.
Forms.
Animations.
Loading states.
Error states.
Accessibility behavior.

Rebuild the interface using independently implemented components.

13.3 Backend limitations

A frontend bundle cannot reveal server-side source code that was never delivered to the client.

AIRE should recover API contracts and observable behavior, then independently reconstruct the backend when sufficient evidence exists.

14. Mobile Application Reconstruction
14.1 Android

Analyze:

APK.
AAB.
DEX.
Manifest.
Resources.
Native libraries.
Signing metadata.
Permissions.
Activities.
Services.
Receivers.
Framework dependencies.

Tools:

JADX.
apktool.
bundletool.
Ghidra.
Native ELF tools.

Reconstruct the managed and native portions independently where required.

14.2 iOS

Analyze:

IPA.
Mach-O.
Info.plist.
Frameworks.
Entitlements.
Assets.
URL schemes.
Provisioning metadata.
Native dependencies.

Recover original resources and source where available.

Use static analysis and authorized testing environments.

14.3 React Native

Investigate:

Hermes.
Metro bundles.
JavaScript.
Native modules.
TurboModules.
Fabric.
Android integration.
iOS integration.
14.4 Flutter

Investigate:

Dart AOT.
Flutter engine.
libapp.
Platform channels.
Plugins.
Assets.
Native integrations.
15. Firmware and Embedded Software

AIRE should investigate:

Firmware containers.
Bootloaders.
Kernels.
Filesystems.
Embedded applications.
Device configuration.
CPU architectures.
Compression.
Partition structures.

Use:

binwalk.
unblob.
UEFITool.
Ghidra.
Filesystem-specific tools.

Extract nested components and analyze each executable using the appropriate architecture-specific tooling.

For encrypted components, document the missing keys or required authorized material rather than claiming successful decryption.

16. Database and Data Structure Recovery

Investigate:

SQLite.
PostgreSQL.
MySQL.
LevelDB.
RocksDB.
Custom databases.
Embedded storage.
Serialized data.

Recover:

Tables.
Columns.
Indexes.
Relationships.
Constraints.
Triggers.
Migrations.
Serialization formats.
Application-level models.

Preserve original databases and companion transaction files.

Use copies for analysis.

17. Protocol and API Reconstruction

Investigate supplied network captures and authorized application interfaces.

Identify:

Protocols.
Message boundaries.
Field types.
Serialization.
Version information.
Request/response relationships.
State transitions.
Error behavior.
Authentication interfaces.
API schemas.

Support formats including:

JSON.
XML.
Protobuf.
FlatBuffers.
Cap'n Proto.
CBOR.
MessagePack.
ASN.1.
Custom binary protocols.

AIRE should create independently implemented protocol parsers and serializers when justified.

Validate reconstructed formats against known authorized test samples.

Do not infer encrypted payload contents from metadata alone.

18. Dynamic Analysis

Static analysis should be preferred when it answers the investigation question.

When runtime behavior needs confirmation, use an isolated and authorized environment.

Investigate:

Process creation.
Filesystem activity.
Library loading.
Network metadata.
IPC.
Database modifications.
Logs.
Exceptions.
Runtime configuration.
State transitions.

Use:

Disposable virtual machines.
Sandboxed containers.
Synthetic data.
Restricted network access.
Snapshot and restore.
Controlled local services.

Record the exact artifact, environment, input, observation method and output.

Distinguish runtime-confirmed facts from static predictions.

19. Automated Source Reconstruction

AIRE should create reconstructed source projects when requested.

19.1 Reconstruction pipeline
text
Recovered Evidence
       |
       v
Architecture Model
       |
       v
Language Identification
       |
       v
Dependency Recovery
       |
       v
Interface Recovery
       |
       v
Data Model Recovery
       |
       v
Algorithm Reconstruction
       |
       v
Source Generation
       |
       v
Build and Compilation
       |
       v
Automated Testing
       |
       v
Compatibility Improvements
       |
       v
Final Source Project

19.2 Reconstruction requirements

Every generated project should include, where applicable:

Source code.
Project files.
Build configuration.
Dependencies.
Resource files.
Configuration examples.
Database schemas.
API definitions.
Tests.
Documentation.
Build instructions.
19.3 Preserve the original architecture where justified

When sufficient evidence exists, reproduce:

Original language.
Original framework.
Original module boundaries.
Original data structures.
Original interfaces.
Original execution model.

When this is impractical, choose a suitable alternative and document the differences.

19.4 Source quality

Generated code should be:

Readable.
Modular.
Documented where useful.
Testable.
Buildable.
Maintainable.
Consistent with recovered behavior.

Do not generate enormous placeholder implementations merely to create the appearance of completeness.

20. Functional Application Cloning

When the user requests a full clone, AIRE should treat the application as a complete system.

20.1 Interface reconstruction

Recover:

Screens.
Pages.
Components.
Navigation.
Dialogs.
Forms.
Controls.
Layouts.
Responsive behavior.
Visual styling.
User interaction.
20.2 Business logic reconstruction

Recover:

Commands.
Services.
Validation.
Algorithms.
Rules.
State transitions.
Background tasks.
Error handling.
20.3 Data reconstruction

Recover:

Data models.
Schemas.
Serialization.
Storage.
Migration behavior.
Import/export functionality.
20.4 Integration reconstruction

Recover observable interfaces for:

APIs.
Local services.
Databases.
Filesystems.
Operating system services.
Authorized external integrations.

Use mock services or independently implemented compatible interfaces when original infrastructure is unavailable.

20.5 Application build

Produce a runnable application for the requested target platform.

Where applicable, support:

macOS.
Windows.
Linux.
Android.
iOS.
Web.
Containers.

AIRE must verify actual build and execution results rather than assuming that generated code works.

21. Compatibility and Behavioral Testing

A working clone must be tested against the original reference wherever authorized access exists.

21.1 Test categories
Unit tests.
Integration tests.
End-to-end tests.
UI tests.
API tests.
Serialization tests.
Database tests.
Regression tests.
Cross-platform tests.
Performance tests.
21.2 Differential testing

Where both applications can be tested safely:

Supply equivalent inputs.
Capture original outputs.
Capture reconstructed outputs.
Normalize irrelevant differences.
Compare results.
Identify mismatches.
Trace the responsible implementation.
Improve the reconstructed code.
Repeat the tests.
21.3 Compatibility scorecard

Report separate scores or statuses for:

Category	Result
Build	Pass / Fail / Not tested
Launch	Pass / Fail / Not tested
Core functionality	Pass / Partial / Fail
UI	Pass / Partial / Fail
API compatibility	Pass / Partial / Fail
Data compatibility	Pass / Partial / Fail
Persistence	Pass / Partial / Fail
Error behavior	Pass / Partial / Fail
Platform compatibility	Pass / Partial / Fail

Do not fabricate numerical compatibility scores.

Only report metrics derived from actual tests.

22. Version Comparison

When multiple versions are available, compare:

File inventories.
Hashes.
Architectures.
Dependencies.
Symbols.
Resources.
Functions.
Data structures.
APIs.
Serialization.
Behavior.

Classify changes as:

Functional.
Dependency-related.
Configuration-related.
Packaging-related.
Compiler-related.
Security-related.
Resource-related.
Unknown.

Distinguish binary changes from observable behavioral changes.

23. AI-Assisted Reverse Engineering

AI should serve as an analysis and reconstruction assistant, not as a substitute for evidence.

Use AI to:

Interpret disassembly.
Explain decompiled functions.
Identify probable algorithms.
Infer data structures.
Correlate functions.
Reconstruct architecture.
Generate parsers.
Generate test cases.
Explain undocumented formats.
Reconstruct source modules.
Suggest alternative implementations.
Investigate compilation errors.
Improve compatibility.
23.1 Evidence-grounded generation

Every important generated implementation should be linked to its supporting evidence.

AI-generated assumptions must be marked explicitly.

23.2 Large application handling

Never attempt to reconstruct an entire large application in one uncontrolled generation step.

Instead:

Build an architecture model.
Identify modules.
Recover module interfaces.
Reconstruct individual components.
Compile and test each component.
Integrate components.
Test complete application workflows.

This makes large reconstructions manageable and reproducible.

23.3 Context management

Persist intermediate findings so analysis can continue across sessions or interrupted runs.

24. Investigation Workflow

AIRE should use the following adaptive lifecycle.

Phase 1: Input discovery

Identify all supplied artifacts and the user's objective.

Phase 2: Fingerprinting

Calculate hashes, sizes, signatures and metadata.

Phase 3: Environment discovery

Detect available tools, runtimes, operating system and architecture.

Phase 4: Tool provisioning

Install missing tools when permitted and verify them.

Phase 5: Recursive extraction

Extract relevant nested containers and inventory their contents.

Phase 6: Format-specific analysis

Route each artifact to appropriate analysis tools.

Phase 7: Source recovery

Search for original source, debug information, source maps and recoverable representations.

Phase 8: Architecture recovery

Reconstruct modules, dependencies, interfaces and execution paths.

Phase 9: Implementation recovery

Analyze relevant functions, algorithms, data models and behavior.

Phase 10: Reconstruction

Generate or independently implement missing functionality when requested.

Phase 11: Build

Compile or package the reconstructed application.

Phase 12: Validation

Run appropriate automated tests and compare against reference behavior.

Phase 13: Improvement

Fix confirmed differences and repeat relevant tests.

Phase 14: Delivery

Provide source code, project files, build instructions, test results and an evidence-backed report.

Not every phase is necessary for every artifact.

25. Environment and Tool Management

AIRE should support:

macOS.
Linux.
Windows.
Containers.
Virtual machines.
Restricted offline environments.

Detect available package managers:

Platform	Package managers
macOS	Homebrew
Debian / Ubuntu	APT
Fedora	DNF
Arch	Pacman
Alpine	APK
Windows	Winget, Chocolatey, Scoop
Python	pip, uv
Node.js	npm, pnpm, yarn
Rust	Cargo
.NET	dotnet tools

Use isolated environments when practical.

Avoid unnecessary administrator privileges.

Never weaken security controls to install a tool.

If installation is unavailable, select an installed alternative or clearly document the limitation.

26. Workspace Structure

Every investigation should use a dedicated workspace.

text
aire/
|
+-- investigations/
|   |
|   +-- artifact-name/
|       |
|       +-- original/
|       +-- extracted/
|       +-- inventory/
|       +-- fingerprints/
|       +-- metadata/
|       +-- strings/
|       +-- symbols/
|       +-- disassembly/
|       +-- decompiled/
|       +-- recovered-source/
|       +-- reconstructed-source/
|       +-- dependencies/
|       +-- databases/
|       +-- protocols/
|       +-- runtime/
|       +-- architecture/
|       +-- comparisons/
|       +-- parsers/
|       +-- builds/
|       +-- tests/
|       +-- reports/
|       +-- logs/
|       |
|       +-- manifest.json
|       +-- source-manifest.json
|       +-- architecture.json
|       +-- dependencies.json
|       +-- compatibility.json
|
+-- tools/
|   +-- installed/
|   +-- downloads/
|   +-- environments/
|
+-- cache/
|
+-- temporary/
|
+-- reports/


Original evidence must remain unchanged.

Generated files must remain separate from recovered original files.

27. Evidence and Accuracy

AIRE must distinguish four fundamental evidence categories.

SEEN

Directly observed in the supplied artifact or recovered files.

INFERRED

A conclusion supported by one or more observations.

RUNTIME-CONFIRMED

Observed during controlled execution.

UNKNOWN

Insufficient evidence exists.

27.1 Confidence

Use:

Confirmed.
Strongly supported.
Tentative.
Unknown.
27.2 Source references

Where possible, include:

File path.
Line number.
Function.
Symbol.
Address.
Offset.
Architecture.
Tool.
Tool version.
27.3 Accuracy requirements

Never:

Invent source code and call it original.
Invent runtime observations.
Fabricate function names.
Claim an application builds without testing.
Claim a clone works without testing.
Assume an unavailable backend has been reconstructed.
Claim complete recovery when information is missing.

Accuracy is more important than appearing successful.

28. Security and Authorization

AIRE is intended for authorized analysis, interoperability, debugging, preservation, defensive research and independent software reconstruction.

Requirements:

Preserve original evidence.
Treat extracted content as untrusted.
Avoid executing unknown software on the host.
Use isolated environments for dynamic analysis.
Use synthetic data where possible.
Protect credentials and sensitive information.
Do not modify production systems.
Do not access third-party systems without authorization.
Do not use reconstructed applications to impersonate services or users.
Respect applicable intellectual property and licensing requirements.

AIRE should favor static analysis, controlled testing and independently implemented functionality.

When a requested operation crosses authorization boundaries, continue with safe analysis and legitimate alternatives.

29. Limitations

AIRE should be ambitious without claiming impossible capabilities.

29.1 Compiled native binaries

A native binary may not contain the original source code.

Decompilation can recover logic, but cannot generally restore comments, formatting, original variable names or exact source organization.

29.2 Encrypted artifacts

Encrypted content cannot be recovered without the required legitimate key or equivalent authorized access.

29.3 Missing server-side implementation

A client application cannot reveal backend source code that was never included in the supplied artifacts.

29.4 External dependencies

Some original functionality may depend on unavailable services, proprietary APIs, hardware or accounts.

AIRE can reconstruct compatible interfaces and controlled substitutes where appropriate.

29.5 Runtime-dependent behavior

Some implementation details only become observable under particular runtime conditions.

Static analysis alone cannot prove that those behaviors occur.

29.6 Irrecoverable information

Information discarded during compilation, compression, transformation or encryption may be impossible to reconstruct exactly.

In such cases, AIRE should implement the closest independently verifiable equivalent.

30. Expected Deliverables

When the user requests a complete reconstruction, AIRE should aim to deliver a complete project rather than a report alone.

Example output:

text
AIRE-RECONSTRUCTION/
|
+-- README.md
|
+-- original-analysis/
|   +-- artifact-manifest.json
|   +-- metadata.json
|   +-- architecture.json
|   +-- dependencies.json
|
+-- recovered-source/
|   +-- original/
|   +-- decompiled/
|
+-- reconstructed-source/
|   +-- src/
|   +-- modules/
|   +-- components/
|   +-- services/
|   +-- models/
|   +-- resources/
|
+-- application/
|   +-- frontend/
|   +-- backend/
|   +-- shared/
|
+-- database/
|   +-- schema/
|   +-- migrations/
|
+-- tests/
|   +-- unit/
|   +-- integration/
|   +-- compatibility/
|   +-- fixtures/
|
+-- build/
|
+-- documentation/
|   +-- ARCHITECTURE.md
|   +-- SOURCE-RECOVERY.md
|   +-- COMPATIBILITY.md
|   +-- LIMITATIONS.md
|
+-- reports/
|   +-- investigation.md
|   +-- findings.md
|   +-- compatibility.json
|
+-- source-manifest.json
+-- manifest.json


Actual project organization should reflect the recovered application architecture rather than blindly following this example.

30.1 Required final report

Include:

What the original artifact is.
What source code was recovered.
What was decompiled.
What was reconstructed.
What could not be recovered.
How the original application works.
What dependencies were identified.
What functionality was implemented.
Whether the project builds.
Whether the application launches.
Which compatibility tests passed.
Which tests failed.
Remaining differences.
Instructions for building and running.
31. Example Usage

AIRE should accept natural-language objectives.

Identify an unknown binary
text
Investigate this binary.

Identify its format, architecture, language,
dependencies and application structure.

Recover all available source-level information.

Recover source code
text
Recover as much of the original source code
as technically possible.

Search for embedded source, source maps,
debug information, symbols and bytecode.

Decompile where necessary.

Preserve original source separately from
generated and reconstructed source.

Reconstruct a complete application
text
Reconstruct this application as a fully
functional independent application.

Recover its architecture, UI, business logic,
data models, dependencies, persistence and
external interfaces.

Generate the source project, build it and
test its functionality against the original
where authorized.

Clone a website
text
Analyze this website and reconstruct its
observable functionality and interface.

Recover available source maps, scripts,
styles, assets, APIs and application state.

Build an independent working implementation.

Compare two binaries
text
Compare these two application versions.

Identify changed functions, dependencies,
resources, interfaces and observable behavior.

Explain the meaningful differences.

Investigate an unknown format
text
Identify this unknown artifact.

Inspect its structure, signatures, offsets,
headers, compression and embedded content.

Find existing parsers or develop a custom
parser if necessary.

Recover a specific feature
text
Investigate how this feature works.

Trace it from the user interaction through
validation, dispatch, implementation, side
effects and result handling.

Reconstruct the feature independently.

32. Configuration

AIRE should support optional investigation preferences.

Example configuration:

json
{
  "aire": {
    "name": "EonaCat AIRE",
    "version": "1.0",
    "mode": "autonomous",
    "objective": "maximum_source_recovery_and_functional_reconstruction"
  },
  "analysis": {
    "automatic_detection": true,
    "recursive_extraction": true,
    "static_analysis": true,
    "dynamic_analysis": "when_authorized_and_required",
    "source_recovery": true,
    "decompilation": true,
    "architecture_recovery": true,
    "dependency_analysis": true
  },
  "reconstruction": {
    "enabled": true,
    "recover_original_source_first": true,
    "generate_missing_source": true,
    "independent_implementation": true,
    "preserve_original_architecture": true,
    "build_application": true,
    "run_tests": true,
    "differential_testing": true
  },
  "tooling": {
    "automatic_discovery": true,
    "automatic_installation": true,
    "verify_installations": true,
    "prefer_official_sources": true,
    "use_isolated_environments": true
  },
  "evidence": {
    "preserve_originals": true,
    "sha256": true,
    "record_tool_versions": true,
    "record_commands": true,
    "track_source_provenance": true,
    "distinguish_original_and_generated": true
  },
  "output": {
    "source_code": true,
    "project_files": true,
    "architecture_report": true,
    "dependency_report": true,
    "test_results": true,
    "compatibility_report": true,
    "build_instructions": true
  }
}


The configuration is illustrative. Actual options depend on the implementation.

33. Roadmap
Phase 1: Universal analysis
Automatic file identification.
Recursive extraction.
Environment discovery.
Tool provisioning.
Metadata extraction.
Dependency detection.
Phase 2: Deep reverse engineering
Native binary analysis.
Managed code decompilation.
Source map recovery.
Debug information recovery.
Architecture reconstruction.
Protocol and database analysis.
Phase 3: Source reconstruction
Automatic source project generation.
Decompiled code organization.
Reconstructed module generation.
Dependency restoration.
Build system generation.
Phase 4: Application reconstruction
UI reconstruction.
Business logic reconstruction.
Database reconstruction.
API compatibility.
Platform-specific builds.
Application packaging.
Phase 5: Autonomous compatibility improvement
Automated test generation.
Differential execution.
Regression testing.
Compatibility reports.
Iterative reconstruction.
Multi-version comparison.
Phase 6: Advanced artifact intelligence
Unfamiliar format investigation.
Custom parser generation.
Cross-language analysis.
Large-project reconstruction.
Advanced architecture correlation.
Persistent investigation state.
34. Final Objective

AIRE is not intended to be a simple file analyzer, decompiler wrapper or metadata extraction utility.

It is intended to be a complete autonomous reverse-engineering and software reconstruction system.

When given an artifact, AIRE should:

Identify what it is.
Understand how it is structured.
Discover the tools needed to analyze it.
Recover all available original source code.
Recover the maximum possible source-level representation.
Understand its dependencies and architecture.
Follow its implementation and execution paths.
Reconstruct missing functionality.
Generate an independent source project.
Build the reconstructed application.
Test its functionality.
Identify compatibility differences.
Improve the implementation.
Deliver the resulting source project and evidence.

The system should always prioritize recovering actual original source where possible.

When exact source recovery is impossible, it should produce the closest accurate reconstruction supported by available evidence.

When a complete application clone is requested, it should aim for a working application rather than merely generating code that looks similar.

The ultimate goal is maximum source recovery, maximum functional compatibility and minimum manual intervention.

EonaCat AIRE

Autonomous Intelligence and Reverse Engineering

Give it an artifact. Recover what exists. Reconstruct what is missing. Verify what works.

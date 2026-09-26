# Requirements

## 1. Project Goal

NeoAI is a privacy-first local AI research agent designed to help
users independently investigate questions, analyze information,
work with documents, use external tools, and build knowledge over time.

NeoAI is designed as a system that supports human reasoning rather
than replacing it.

The system should help users:

- investigate questions using diverse sources
- examine information that may conflict with their existing beliefs
- identify contradictions and disagreements
- distinguish claims from the evidence presented for those claims
- inspect the origin and context of information
- analyze documents and other forms of data
- work across multiple languages
- perform structured analysis when explicitly requested
- maintain private, user-controlled knowledge and memory
- use local AI models whenever possible
- maintain control over personal data, tools, networking, and system
  capabilities

NeoAI should be capable of building persistent knowledge,
learning from previous interactions, and improving its workflows
over time while remaining under user control.


## 2. Core Principles

### 2.1 Privacy First

NeoAI MUST prioritize user privacy and data ownership.

Private user data MUST remain under the user's control.

Personal conversations, memories, documents, credentials, and other
sensitive information MUST NOT be sent to external services unless
the user explicitly enables and authorizes such behavior.

### 2.2 Local First

NeoAI SHOULD perform AI inference, memory management, and data
processing locally whenever technically possible.

External services SHOULD be optional rather than required for the
core functionality of the system.

### 2.3 User Control

The user MUST remain in control of NeoAI's data, tools, networking,
permissions, and significant system capabilities.

NeoAI MUST NOT silently grant itself new privileges or unrestricted
access to the host system.

### 2.4 Transparency

NeoAI SHOULD make its actions understandable to the user.

The system SHOULD clearly indicate:

- what tools it used
- what sources it accessed
- what files it accessed
- what external services it contacted
- what actions it performed
- what information was stored in memory
- when uncertainty or missing information affects the result

### 2.5 Modularity

NeoAI MUST be designed as a modular system.

Major components SHOULD be replaceable without requiring the entire
system to be rewritten.

This includes, where practical:

- AI model providers
- memory backends
- search providers
- document processors
- networking components
- tools
- user interfaces

### 2.6 Human Oversight

NeoAI SHOULD be capable of operating autonomously within clearly
defined boundaries.

Actions that may create significant security, privacy, financial,
system, or external-world consequences SHOULD require explicit user
approval.

### 2.7 Reproducibility

Important research results SHOULD be reproducible whenever practical.

NeoAI SHOULD retain sufficient information about the research process,
sources, tools, and relevant inputs to allow the user to understand
how a result was produced.


## 3 Internal Reasoning and Conclusions

NeoAI SHOULD be capable of forming its own conclusions through
analysis of collected evidence, documents, data, previous research,
and other available information.

NeoAI MAY maintain internal assessments or conclusions even when they
are not presented to the user.

NeoAI SHOULD NOT automatically present its internal conclusions as
the answer to a research question.

When Research Mode is being used, NeoAI SHOULD primarily present the
underlying research material and allow the user to form their own
conclusions.

NeoAI SHOULD present its own analysis or conclusions when the user
explicitly asks for them.

When presenting its own conclusion, NeoAI MUST distinguish its
analysis from the underlying source material and MUST explain the
main evidence and reasoning on which the conclusion is based.

NeoAI SHOULD acknowledge significant uncertainty, contradictory
evidence, or limitations in the available material when they affect
its conclusion.


## 4. Research Mode

Research Mode is the primary research mode of NeoAI.

Its purpose is to help the user investigate a question by collecting,
organizing, comparing, and presenting relevant information and sources.

### 4.1 Research Process

When conducting research, NeoAI SHOULD:

1. understand and define the research question
2. identify important terms, assumptions, and ambiguities
3. create an appropriate research strategy
4. search for relevant sources
5. identify primary and secondary sources
6. extract relevant claims, evidence, and supporting information
7. search for evidence that supports the claims
8. actively search for evidence that contradicts or challenges the claims
9. identify disagreements between sources
10. investigate the origin and relationship of relevant sources
11. distinguish evidence from interpretation and opinion
12. identify unresolved questions and uncertainty
13. present the collected material with source references
14. provide a structured research summary

### 4.2 Research Independence

Research Mode MUST NOT be designed solely to confirm the user's
initial assumptions.

NeoAI SHOULD actively search for information that may challenge the
initial assumptions or conclusions of the research.

NeoAI SHOULD investigate relevant minority, controversial, or
alternative claims when they are materially relevant to the research
question.

The inclusion of a claim in the research results MUST NOT be treated
as an endorsement of that claim.

### 4.3 Source Diversity

NeoAI SHOULD use multiple relevant sources when the research question
requires it.

When practical, NeoAI SHOULD prioritize direct and primary evidence
while also considering relevant secondary sources.

NeoAI SHOULD identify when multiple sources appear to rely on the
same underlying information.

NeoAI MUST NOT treat the number of sources supporting a claim as
sufficient evidence of its validity.

### 4.4 Contradictions

When sources disagree, NeoAI SHOULD explicitly identify the
disagreement.

NeoAI SHOULD explain:

- what the sources disagree about
- what evidence each side presents
- whether the disagreement concerns facts, interpretation,
  methodology, terminology, or other factors
- whether additional evidence can help resolve the disagreement
- what remains unresolved

NeoAI MUST NOT hide relevant contradictions simply because they make
the research result more complicated.

### 4.5 Research Output

A Research Mode result SHOULD contain, when applicable:

- research question
- research strategy
- relevant sources
- source type and provenance
- important claims
- supporting evidence
- contradictory evidence
- source criticism
- unresolved questions
- uncertainty and limitations
- structured summary
- references to the underlying sources

Research Mode SHOULD allow the user to inspect the underlying
material rather than only presenting a generated summary.

### 4.6 Research Depth

NeoAI SHOULD adapt the depth of research to the complexity and
importance of the question.

Simple factual questions MAY require only limited research.

Complex, controversial, or highly disputed questions SHOULD trigger
deeper research, broader source comparison, and more extensive
investigation.

NeoAI SHOULD indicate when the available research is insufficient to
support a reliable conclusion.


## 5. Analysis Mode

Analysis Mode is an optional capability of NeoAI that allows the
system to analyze collected information, documents, data, and
research results and form its own reasoned conclusions.

Analysis Mode MUST NOT replace Research Mode.

Research Mode remains the primary mechanism for independent
investigation and collection of source material.

### 5.1 Independent Analysis

NeoAI SHOULD be capable of forming its own conclusions by analyzing:

- research results
- source material
- documents
- structured and unstructured data
- information stored in its knowledge base
- previous research
- information provided directly by the user

NeoAI MAY maintain internal assessments or conclusions without
automatically presenting them to the user.

NeoAI SHOULD NOT automatically present its own conclusions when the
user has requested Research Mode unless the user asks for an analysis
or conclusion.

### 5.2 User-Requested Conclusions

When the user explicitly asks NeoAI for its own assessment,
interpretation, or conclusion, NeoAI MAY provide one.

The conclusion MUST be clearly distinguished from the underlying
source material.

NeoAI SHOULD explain:

- the main evidence supporting the conclusion
- the reasoning used to reach the conclusion
- significant evidence that contradicts or weakens the conclusion
- relevant uncertainty and limitations

NeoAI MUST NOT present its own analytical conclusion as an
indisputable fact.

### 5.3 Source-Based Reasoning

NeoAI SHOULD base its conclusions on available evidence rather than
on unsupported assumptions.

When possible, each significant conclusion SHOULD be traceable to
the relevant source material or evidence used to reach it.

NeoAI SHOULD distinguish between:

- information directly supported by sources
- interpretation of that information
- inference made by NeoAI
- unresolved uncertainty

### 5.4 Learning From Analysis

NeoAI SHOULD be capable of learning from analyzed information and
research.

When information is added to persistent knowledge, NeoAI SHOULD
preserve its provenance and context, including where the information
came from and, when applicable, what analysis led to the conclusion.

NeoAI MUST NOT treat its previous conclusions as automatically
correct.

Previous conclusions SHOULD remain open to revision when new evidence
or contradictory information becomes available.


## 6. Source Handling and Evidence

NeoAI MUST preserve the relationship between information, claims,
evidence, sources, interpretations, and conclusions.

NeoAI MUST distinguish between:

- the source itself
- a claim made by the source
- evidence presented by the source
- interpretation of the evidence
- criticism of the source or evidence
- conclusions produced by NeoAI

### 6.1 Source Provenance

NeoAI SHOULD record, whenever available:

- source title
- author or organization
- publication date
- source type
- original location
- language
- publication context
- referenced sources
- relevant metadata

NeoAI SHOULD preserve enough provenance information to allow the
user to locate and inspect the original source.

### 6.2 Primary and Secondary Sources

NeoAI SHOULD distinguish between primary and secondary sources.

Primary sources SHOULD be given particular attention when they are
directly relevant to the research question.

Secondary sources MAY be used to provide context, interpretation,
analysis, or references to additional material.

NeoAI MUST NOT assume that a primary source is automatically correct
or that a secondary source is automatically unreliable.

### 6.3 Source Relationships

NeoAI SHOULD identify when multiple sources:

- cite the same underlying source
- reproduce substantially the same information
- depend on the same dataset
- derive information from the same testimony or document
- independently provide similar evidence

NeoAI SHOULD avoid presenting multiple dependent sources as fully
independent confirmation.

### 6.4 Claims and Evidence

NeoAI MUST distinguish between a claim and the evidence supporting
that claim.

For significant claims, NeoAI SHOULD identify:

- who makes the claim
- what evidence is presented
- what evidence supports it
- what evidence challenges it
- how the evidence was obtained
- whether the evidence can be directly inspected
- what assumptions are required to interpret the evidence

### 6.5 Source Criticism

NeoAI SHOULD identify relevant criticism of sources, evidence, and
methodologies.

Criticism MUST be attributed to its source.

NeoAI MUST NOT reject or suppress a source solely because another
source describes it as propaganda, misinformation, disinformation,
unreliable, controversial, or unverifiable.

Instead, NeoAI SHOULD present the criticism and the reasoning or
evidence behind it when relevant.

### 6.6 Conflicting Evidence

When relevant evidence conflicts, NeoAI SHOULD present the
conflicting evidence rather than silently selecting one side.

NeoAI SHOULD explain the nature of the conflict and identify what
additional information could potentially resolve it.

### 6.7 Source Transparency

Research results SHOULD provide direct references to the sources used.

When technically possible, users SHOULD be able to inspect the
relevant source material underlying important claims and conclusions.

NeoAI SHOULD make clear when information could not be independently
checked because the original source was unavailable, inaccessible,
deleted, paywalled, or otherwise limited.


## 7. Local AI

NeoAI SHOULD prioritize local AI models and local inference.

The system MUST be designed to operate without requiring a permanently
connected external AI service for its core functionality.

NeoAI SHOULD support multiple AI model providers rather than being
permanently tied to a single model or vendor.

The initial implementation SHOULD support local models through a
locally available inference server such as LM Studio.

The AI model layer SHOULD be replaceable without requiring changes to
the rest of the NeoAI architecture.

NeoAI SHOULD support models with different capabilities and sizes
depending on the available hardware.

The system SHOULD detect or allow configuration of model capabilities
and hardware limitations where practical.

Private user data SHOULD be processed locally whenever possible.

When an external AI service is used, NeoAI MUST clearly identify that
external processing is taking place and SHOULD require explicit user
authorization unless the user has previously configured such access.

NeoAI MUST NOT assume that a specific AI model is permanently
available or sufficient for all tasks.

The system SHOULD allow different models to be used for different
tasks when technically practical.


## 8. Memory

NeoAI SHOULD maintain persistent local memory that allows the system
to retain useful information across interactions.

Memory MUST remain under the user's control.

NeoAI SHOULD distinguish between different types of memory, including:

- short-term conversational context
- long-term user preferences
- learned knowledge
- research results
- source and evidence relationships
- previous analyses and conclusions
- learned workflows and skills
- system configuration and operational information

### 8.1 Memory Provenance

NeoAI SHOULD preserve the origin and context of important stored
information.

When applicable, stored knowledge SHOULD include:

- source
- date
- context
- supporting evidence
- contradictory evidence
- related research
- previous analysis
- current assessment

NeoAI SHOULD NOT store important conclusions without preserving
sufficient information about their origin.

### 8.2 Memory Revision

NeoAI MUST be capable of revising previously stored knowledge when
new evidence contradicts or significantly changes an earlier
conclusion.

New information SHOULD NOT automatically overwrite previous
information when doing so would destroy useful historical context.

NeoAI SHOULD preserve relevant changes to important knowledge over
time.

### 8.3 User Memory

NeoAI MAY remember user preferences, instructions, recurring
workflows, and other information that improves future interactions.

The user MUST remain in control of persistent personal memory.

NeoAI SHOULD avoid storing unnecessary sensitive or personal
information.

### 8.4 Research Memory

NeoAI SHOULD be capable of storing completed research in a structured
form.

Research memory SHOULD preserve:

- research question
- sources
- claims
- evidence
- contradictions
- analysis
- conclusions
- uncertainty
- date of research

This should allow NeoAI to revisit previous research when new
questions or evidence appear.

### 8.5 Learning From Memory

NeoAI SHOULD use relevant previous knowledge and research when
appropriate.

Previous memory MUST NOT automatically be treated as unquestionable
truth.

NeoAI SHOULD be capable of recognizing when new evidence conflicts
with stored knowledge and should be able to re-evaluate the relevant
information.


## 9. Documents and Languages

NeoAI SHOULD be capable of processing and analyzing documents and
other user-provided data locally whenever technically possible.

### 9.1 Supported Documents

NeoAI SHOULD support, where technically practical:

- TXT
- Markdown
- PDF
- DOCX
- CSV
- JSON
- HTML
- images
- scanned documents

The document processing system SHOULD be modular so that additional
formats can be added without redesigning the entire system.

### 9.2 Document Analysis

NeoAI SHOULD be capable of:

- summarizing documents
- answering questions about documents
- extracting information
- searching within documents
- identifying important passages
- comparing multiple documents
- identifying contradictions between documents
- extracting structured data
- translating documents
- explaining complex documents
- identifying relevant metadata
- referencing the location of important information within a document
  when technically possible

When possible, NeoAI SHOULD preserve document structure and
provenance when extracting information.

### 9.3 Document Research

Documents SHOULD be usable as research sources.

NeoAI SHOULD be capable of combining user-provided documents with
external research when authorized by the user.

User-provided documents MUST NOT be automatically published,
uploaded, or shared with external services without explicit
authorization.

### 9.4 Multilingual Support

NeoAI SHOULD support multiple languages for:

- conversation
- research
- document analysis
- translation
- source processing
- information extraction

NeoAI SHOULD be capable of researching a topic using sources written
in different languages.

When researching multilingual topics, NeoAI SHOULD preserve the
original source language and provide translations when requested.

Translations SHOULD NOT replace the original source when the original
text is important for interpreting the evidence.

### 9.5 Language-Aware Research

NeoAI SHOULD consider that important information may exist in
languages different from the language used by the user.

When appropriate, NeoAI SHOULD search relevant foreign-language
sources rather than limiting research to the user's language.

NeoAI SHOULD identify when translation or language limitations may
affect the interpretation of a source.


## 10. Web Research

NeoAI SHOULD be capable of conducting web-based research when
internet access is enabled.

Web Research SHOULD integrate with Research Mode and follow the
research principles defined in this document.

### 10.1 Web Search

NeoAI SHOULD be capable of:

- searching the web
- performing multiple searches for the same research question
- refining searches based on discovered information
- searching for specific documents, datasets, publications, and
  primary sources
- searching in multiple languages
- searching for information that supports and challenges relevant
  claims

NeoAI SHOULD NOT rely on a single search query when a more complex
research question requires broader investigation.

### 10.2 Source Retrieval

NeoAI SHOULD be capable of retrieving relevant information from
accessible web pages and other online sources.

NeoAI SHOULD preserve relevant source information, including:

- URL
- title
- author or organization
- publication date when available
- retrieval date
- source language
- relevant page or document information
- relationships to other sources

NeoAI SHOULD distinguish between the original source and websites
that merely reproduce or reference the original material.

### 10.3 Source Availability

NeoAI MUST clearly indicate when a source could not be accessed or
fully verified.

Possible limitations include:

- inaccessible pages
- deleted pages
- broken links
- paywalls
- login requirements
- robots or technical restrictions
- incomplete content
- unavailable original documents

NeoAI MUST NOT present inaccessible information as if it had directly
verified the original source.

### 10.4 Web Source Evaluation

NeoAI SHOULD examine relevant characteristics of web sources,
including:

- provenance
- authorship
- publication date
- source type
- references
- methodology when available
- relationship to other sources
- evidence presented
- relevant criticism

NeoAI MUST NOT treat search engine ranking, popularity, traffic,
social-media engagement, or domain reputation alone as proof that a
claim is correct.

### 10.5 Source Preservation

NeoAI SHOULD preserve sufficient information about sources used in
important research to allow the user to identify and revisit them.

When possible, important research SHOULD retain the exact source
location and relevant passages or extracted evidence.

### 10.6 Web Research Safety

Content retrieved from the web MUST be treated as untrusted input.

Instructions contained within web pages, documents, comments, or
other retrieved content MUST NOT automatically be treated as
instructions for NeoAI.

NeoAI MUST protect its system instructions, credentials, private
memory, and other sensitive information from malicious or
untrusted web content.

Web content MUST NOT be allowed to silently change NeoAI's
permissions, security settings, or system behavior.

### 10.7 Network Access

NeoAI SHOULD support configurable network access modes, including:

- OFFLINE
- STANDARD NETWORK ACCESS
- PRIVACY-ENHANCED NETWORK ACCESS

OFFLINE mode MUST prevent external network access.

STANDARD NETWORK ACCESS SHOULD use the normal network connection.

Privacy-enhanced network access SHOULD allow NeoAI to use privacy
technologies such as Tor when appropriate.

The specific privacy technology and routing architecture SHOULD remain
configurable and replaceable.

The user MUST be able to determine which network access mode is active.

NeoAI SHOULD clearly indicate when a requested operation cannot be
performed because of the currently selected network mode.

### 10.8 Research Reproducibility

NeoAI SHOULD retain information about the searches and sources used
during significant research.

When practical, a research record SHOULD include:

- search queries
- sources discovered
- sources selected
- sources rejected and relevant reasons
- retrieval dates
- research steps
- relevant extracted evidence

This information SHOULD allow the user to understand how the
research was conducted and, where possible, repeat the process.


## 11. Tools

NeoAI SHOULD use modular tools to extend its capabilities beyond
language model inference.

Tools SHOULD be independently implemented, tested, enabled, disabled,
and replaced.

NeoAI SHOULD initially support or be designed to support tools such
as:

- calculator
- date and time
- filesystem access
- document processing
- web search
- web page retrieval
- structured data processing
- Python or other controlled code execution
- translation
- text extraction
- OCR

### 11.1 Tool Permissions

Tools MUST operate within clearly defined permissions.

NeoAI MUST NOT have unrestricted access to the host operating system
by default.

Filesystem access SHOULD be limited to explicitly permitted
locations.

Network access SHOULD follow the currently selected network mode.

Code execution MUST be isolated or otherwise appropriately
restricted.

### 11.2 Tool Selection

NeoAI SHOULD be capable of determining when a tool is appropriate
for a task.

NeoAI SHOULD NOT use a tool when the task can be completed safely
and reliably without it.

NeoAI SHOULD identify which tools were used when transparency is
relevant.

### 11.3 Tool Results

Tool output MUST be treated as external input and SHOULD be validated
before being used in further reasoning.

NeoAI SHOULD distinguish between information generated by the model
and information returned by a tool.

Tool failures MUST NOT be silently presented as successful results.

### 11.4 User Approval

Low-risk tool operations MAY be performed automatically.

Operations that may affect important data, system configuration,
security, privacy, external services, or other significant resources
SHOULD require explicit user approval.

NeoAI SHOULD clearly explain what action requires approval before
requesting it.

### 11.5 Tool Extensibility

The tool system SHOULD allow new capabilities to be added without
modifying the core reasoning system.

Tools SHOULD expose clearly defined interfaces so that NeoAI can
interact with them in a predictable and testable way.


## 12. Skills and Self-Improvement

NeoAI SHOULD support a modular skill system that allows the system
to expand its capabilities over time.

Skills SHOULD represent reusable capabilities or workflows that NeoAI
can use to perform specific types of tasks.

Examples may include:

- research workflows
- document analysis
- translation
- data analysis
- troubleshooting
- system administration
- programming assistance
- source comparison
- information extraction

### 12.1 Skill Structure

Skills SHOULD be modular and independently maintainable.

A skill SHOULD define:

- its purpose
- required tools
- required permissions
- expected inputs
- expected outputs
- limitations
- dependencies
- safety considerations

### 12.2 Skill Discovery

NeoAI SHOULD be capable of identifying situations where an existing
skill could improve the result.

NeoAI MAY suggest creating or improving a skill when it repeatedly
encounters the same type of task or limitation.

### 12.3 Skill Creation

NeoAI MAY assist in designing or creating new skills.

New skills MUST NOT automatically receive unrestricted permissions.

Skills that require significant new capabilities, permissions,
network access, filesystem access, or external services SHOULD
require explicit user approval before activation.

### 12.4 Learning From Experience

NeoAI SHOULD be capable of learning from previous interactions,
research, tool usage, errors, and successful workflows.

NeoAI SHOULD identify recurring mistakes and opportunities to improve
its workflows.

Learning SHOULD preserve relevant context and provenance where
practical.

### 12.5 Self-Improvement

NeoAI SHOULD be capable of proposing improvements to its own
workflows, tools, skills, or reasoning processes.

NeoAI MUST NOT silently modify critical system components,
permissions, security mechanisms, or its own core architecture.

Significant self-modifications SHOULD require explicit user approval.

### 12.6 Human Control

The user MUST remain in control of which skills are installed,
enabled, disabled, modified, or removed.

NeoAI SHOULD clearly communicate when a proposed skill would introduce
new permissions, dependencies, or security risks.


## 13. Privacy and Data Protection

NeoAI MUST treat user data as private by default.

The system SHOULD minimize the amount of personal and sensitive data
that is collected, stored, processed, or transmitted.

### 13.1 Local Data

Private conversations, memories, documents, research history,
configuration, credentials, and other sensitive user data SHOULD be
stored locally whenever technically possible.

Private data MUST NOT be included in the public NeoAI repository.

Private data MUST NOT be uploaded to external services unless the
user has explicitly authorized the relevant operation.

### 13.2 External Services

When NeoAI sends data to an external service, the system SHOULD make
the destination and purpose of the transfer clear.

NeoAI SHOULD minimize the amount of data sent to external services.

Where technically practical, NeoAI SHOULD process or sanitize data
locally before sending it externally.

External AI models, search providers, APIs, cloud storage, and other
third-party services SHOULD be treated as separate trust boundaries.

### 13.3 Credentials and Secrets

Passwords, API keys, authentication tokens, private keys, session
tokens, and other secrets MUST NOT be stored directly in source code.

Secrets MUST NOT be committed to the public Git repository.

NeoAI SHOULD use appropriate local secret storage or environment-based
configuration where practical.

### 13.4 Personal Documents

User-provided documents MUST be treated as private data by default.

NeoAI MUST NOT automatically publish, upload, index externally, or
share private documents without explicit authorization.

Document access SHOULD be limited to the permissions required for the
requested task.

### 13.5 Memory Privacy

Persistent memory MUST remain under the user's control.

NeoAI SHOULD allow the user to understand what information is being
stored as persistent memory.

Sensitive information SHOULD NOT be stored unnecessarily.

Memory used for research or reasoning SHOULD retain provenance without
unnecessarily storing unrelated personal information.

### 13.6 Logs

Logs SHOULD contain enough information to diagnose problems,
understand system behavior, and audit important actions.

Logs MUST NOT unnecessarily contain passwords, authentication tokens,
private documents, or other sensitive information.

NeoAI SHOULD provide mechanisms for reducing or anonymizing sensitive
information in logs where practical.

### 13.7 Data Isolation

Different categories of data SHOULD be logically separated where
practical.

This may include:

- conversations
- personal memory
- research data
- documents
- credentials
- system configuration
- logs
- temporary data

A component that does not require access to a particular category of
data SHOULD NOT receive that access.

### 13.8 Data Lifecycle

NeoAI SHOULD define how data is created, stored, modified, archived,
and deleted.

Temporary data SHOULD NOT be retained indefinitely without a reason.

The user SHOULD be able to remove persistent personal data and
research data when appropriate.

### 13.9 Privacy by Default

Privacy-preserving behavior SHOULD be the default configuration.

Features that increase external data exposure SHOULD require explicit
configuration or authorization unless the user has intentionally
enabled them as a persistent preference.


## 14. Networking

NeoAI SHOULD be capable of operating in different networking
environments depending on the user's requirements and configuration.

### 14.1 Offline Operation

NeoAI SHOULD be capable of operating without an internet connection
for functionality that does not require external data.

Core local functionality SHOULD remain available in Offline mode.

NeoAI MUST NOT attempt to establish external network connections when
Offline mode is active.

### 14.2 Local Network

NeoAI SHOULD support communication with other authorized devices on
the user's local network.

This MAY allow devices such as:

- smartphones
- tablets
- laptops
- desktop computers

to access a NeoAI instance running on another authorized device.

Local network access SHOULD use appropriate authentication and
security mechanisms.

### 14.3 Remote Access

NeoAI SHOULD be capable of supporting secure remote access when
explicitly configured by the user.

Remote access MUST NOT expose NeoAI's administrative interfaces or
private data by default.

Remote connections SHOULD use appropriate encryption,
authentication, and access controls.

### 14.4 Network Separation

NeoAI SHOULD separate different types of network traffic where
practical.

Examples include:

- public source retrieval
- private user communication
- model provider communication
- system updates
- administrative access

Different traffic types MAY use different network routes or security
policies.

### 14.5 Network Permissions

Network access SHOULD follow the permissions and network mode
configured by the user.

NeoAI MUST NOT silently bypass configured network restrictions.

Tools and skills SHOULD inherit appropriate network restrictions
rather than automatically receiving unrestricted network access.

### 14.6 Network Failure

NeoAI SHOULD handle network failures gracefully.

If an external service becomes unavailable, NeoAI SHOULD:

- report the failure clearly
- avoid presenting incomplete results as complete
- preserve already collected information when appropriate
- continue locally when possible

### 14.7 Replaceable Network Architecture

The networking layer SHOULD be modular.

NeoAI SHOULD be capable of supporting different networking and privacy
technologies without requiring changes to the core reasoning,
memory, or research systems.


## 15. Public and Private Architecture

NeoAI SHOULD separate publicly distributable project components from
private user data, configuration, credentials, and deployment-specific
components.

### 15.1 Public Components

The public NeoAI repository MAY contain:

- source code intended for distribution
- documentation
- tests
- examples
- public configuration templates
- architecture documentation
- security documentation
- development tools
- non-sensitive sample data

### 15.2 Private Components

Private NeoAI data and components MAY include:

- personal memory
- conversations
- private research history
- private documents
- credentials
- API keys
- authentication tokens
- private configuration
- local databases
- private logs
- deployment-specific secrets
- other sensitive user data

Private data MUST NOT be committed to the public repository.

### 15.3 Configuration Separation

NeoAI SHOULD separate public configuration templates from private
configuration.

Public configuration SHOULD contain only safe defaults and examples.

Private configuration SHOULD be stored locally and MUST NOT contain
secrets that are committed to the public repository.

### 15.4 Local Extensions

NeoAI SHOULD allow users to maintain private local extensions,
modules, skills, tools, or configurations without requiring them to be
published publicly.

Private extensions SHOULD be capable of interacting with the public
NeoAI architecture through defined interfaces where practical.

### 15.5 Deployment Independence

The public NeoAI codebase SHOULD remain usable without requiring
access to the creator's private data, memory, credentials, or
infrastructure.

Private deployment-specific components SHOULD NOT be required for the
basic operation of the public project.

### 15.6 Data Boundaries

NeoAI SHOULD maintain clear boundaries between:

- public project code
- private user data
- secrets and credentials
- temporary runtime data
- external services
- deployment-specific configuration

These boundaries SHOULD be enforced through technical mechanisms
where practical rather than relying only on user discipline.


## 16. GitHub

GitHub SHOULD be used as the primary public platform for development,
version control, documentation, and collaboration for the public NeoAI
project.

### 16.1 Public Repository

The public repository MAY contain:

- source code
- documentation
- tests
- examples
- architecture documentation
- requirements
- security documentation
- development guidelines
- non-sensitive configuration templates

### 16.2 Private Data Protection

The public GitHub repository MUST NOT contain:

- personal conversations
- private memory
- private research history
- private documents
- passwords
- API keys
- authentication tokens
- private keys
- sensitive logs
- personal configuration
- other private user data

NeoAI SHOULD provide appropriate mechanisms such as configuration
templates and `.gitignore` rules to reduce the risk of accidentally
committing private data.

### 16.3 Version Control

NeoAI development SHOULD use version control to track changes to the
project.

Significant changes SHOULD be committed with clear commit messages.

Changes SHOULD be tested before being committed when practical.

### 16.4 Public Development

The public repository SHOULD document the development process and
architecture clearly enough for other developers to understand,
review, test, and contribute to the project.

Security-sensitive implementation details SHOULD be documented
carefully without exposing secrets or unnecessarily increasing the
risk of abuse.

### 16.5 GitHub Access

NeoAI MAY interact with GitHub through dedicated tools in the future.

GitHub access SHOULD be treated as a separate permission from general
web access.

NeoAI MUST NOT automatically publish code, research, memory, private
data, or other content to GitHub without appropriate authorization.

### 16.6 Repository Integrity

NeoAI SHOULD protect the integrity of the project repository.

Automated changes to the public repository SHOULD be reviewable and
traceable.

NeoAI SHOULD NOT silently modify or publish project files without
appropriate authorization.


## 17. Security

Security MUST be treated as a core requirement of NeoAI.

NeoAI SHOULD follow the principles of least privilege, explicit
permissions, isolation, and defense in depth.

### 17.1 Threats

NeoAI SHOULD be designed to defend against threats including:

- malicious web pages
- prompt injection
- malicious documents
- malicious tool output
- malicious or compromised external services
- unauthorized filesystem access
- unauthorized network access
- credential and secret leakage
- accidental data exposure
- malicious skills or extensions
- unsafe code execution
- unauthorized modification of system components
- manipulation of persistent memory

### 17.2 Least Privilege

NeoAI MUST NOT receive more permissions than required for a task.

Tools, skills, processes, and external services SHOULD receive only
the access necessary for their intended purpose.

Permissions SHOULD be isolated between components where practical.

### 17.3 Untrusted Input

External content MUST be treated as potentially untrusted.

This includes:

- web pages
- downloaded files
- documents
- emails
- tool results
- external API responses
- user-provided data

Untrusted content MUST NOT automatically gain the ability to modify
NeoAI's instructions, permissions, configuration, memory, or system
behavior.

### 17.4 Code Execution

Code execution MUST be treated as a high-risk capability.

NeoAI SHOULD isolate executed code from sensitive system resources.

Code execution SHOULD have clearly defined:

- filesystem permissions
- network permissions
- resource limits
- execution time limits
- available libraries or capabilities

### 17.5 Memory Security

NeoAI MUST protect persistent memory from unauthorized modification
or extraction.

Untrusted external content MUST NOT be allowed to silently write
arbitrary information into trusted persistent memory.

Important memory updates SHOULD have identifiable provenance.

### 17.6 Permission Changes

Changes to important permissions, security settings, network access,
or system capabilities SHOULD require explicit user approval.

NeoAI MUST NOT silently escalate its own privileges.

### 17.7 Security Failures

When a security-sensitive operation fails or cannot be performed
safely, NeoAI SHOULD fail safely rather than bypassing the security
restriction.

Security failures SHOULD be clearly reported to the user.

### 17.8 Security Updates

Security-sensitive components SHOULD be kept updateable independently
where practical.

NeoAI SHOULD provide mechanisms for identifying known security issues
in its own dependencies and components.


## 18. Auditability

NeoAI SHOULD maintain appropriate audit information about important
system actions.

Audit information SHOULD help the user understand what NeoAI did,
which tools and sources it used, and what relevant decisions or
changes occurred.

### 18.1 Actions

When practical, NeoAI SHOULD record important actions such as:

- tool usage
- web searches
- source retrieval
- document access
- memory updates
- skill activation
- permission changes
- external service usage
- code execution
- significant configuration changes
- security-related events
- errors and failures

### 18.2 Research Audit Trail

Important research SHOULD retain an audit trail containing relevant
information about:

- research questions
- search queries
- sources discovered
- sources used
- relevant evidence
- research steps
- retrieval dates
- significant tool usage
- analysis performed

The audit trail SHOULD allow the user to understand how important
research results were produced.

### 18.3 Privacy

Audit logs MUST NOT unnecessarily contain sensitive information.

Passwords, authentication tokens, private keys, and other secrets
MUST NOT be stored in audit logs.

Private documents and conversations SHOULD NOT be copied into logs
unless necessary for a specific purpose.

### 18.4 Memory and Knowledge Changes

Important changes to persistent memory and knowledge SHOULD be
traceable.

When practical, NeoAI SHOULD record:

- what information was changed
- why it was changed
- what source or event caused the change
- when the change occurred
- whether the change was automatic or user-approved

### 18.5 User Visibility

The user SHOULD be able to inspect relevant audit information.

NeoAI SHOULD provide understandable explanations of important actions
without requiring the user to inspect raw technical logs.

### 18.6 Audit Integrity

Audit information SHOULD be protected from unauthorized modification
or deletion.

Security-relevant audit records SHOULD be sufficiently reliable to
support investigation of unexpected behavior or security incidents.


## 19. User Interface

NeoAI SHOULD provide a clear and understandable interface for
interacting with the system.

### 19.1 Initial Interface

The initial implementation SHOULD prioritize a simple interface that
allows the user to:

- communicate with NeoAI
- perform research
- request analysis
- provide documents
- inspect sources
- inspect relevant research results
- manage basic configuration
- view important system messages and errors

A command-line interface MAY be used during early development.

### 19.2 Research Interface

The interface SHOULD clearly distinguish between:

- user input
- source material
- research results
- evidence
- NeoAI analysis
- uncertainty
- system-generated information

Research results SHOULD allow the user to inspect the underlying
sources rather than only viewing generated summaries.

### 19.3 Tool Transparency

The interface SHOULD make important tool usage visible to the user.

When relevant, the user SHOULD be able to determine:

- which tools were used
- which sources were accessed
- which files were accessed
- whether external services were contacted
- whether an operation requires approval

### 19.4 Privacy and Security

The interface SHOULD clearly communicate important privacy and
security states.

The user SHOULD be able to determine:

- current network mode
- relevant permissions
- external service usage
- important pending approvals
- security warnings
- significant errors

### 19.5 Future Interfaces

NeoAI MAY eventually provide additional interfaces, including:

- web interface
- desktop application
- mobile interface
- research dashboard
- memory browser
- tool management interface
- security and permissions dashboard

Additional interfaces SHOULD use the same underlying NeoAI
architecture rather than creating separate implementations of the core
reasoning system.


## 20. Performance and Resource Management

NeoAI SHOULD be designed to operate efficiently within the hardware
resources available to the user.

### 20.1 Resource Awareness

NeoAI SHOULD be aware of relevant system limitations, including:

- CPU resources
- available memory
- GPU resources
- available storage
- network availability
- model resource requirements

NeoAI SHOULD avoid unnecessary consumption of system resources.

### 20.2 Model Selection

NeoAI SHOULD allow different models to be selected based on the
available hardware and the requirements of the task.

The system SHOULD avoid loading models or components that exceed
available system resources when this can be detected in advance.

### 20.3 Task Prioritization

NeoAI SHOULD prioritize tasks according to their importance and
resource requirements when multiple operations are running.

Long-running or resource-intensive operations SHOULD provide
appropriate status information to the user.

### 20.4 Graceful Degradation

When available resources are insufficient for a requested operation,
NeoAI SHOULD attempt to degrade gracefully.

Possible approaches MAY include:

- using a smaller model
- reducing context size
- processing data in smaller batches
- disabling non-essential components
- asking the user for approval before starting a resource-intensive
  operation

NeoAI MUST NOT silently terminate or corrupt important user data due
to predictable resource limitations.

### 20.5 Background Operations

Background operations SHOULD be configurable.

The user SHOULD be able to determine which tasks may run
automatically in the background.

Resource-intensive background operations SHOULD NOT significantly
interfere with normal system usage without appropriate configuration
or user approval.

### 20.6 Resource Monitoring

NeoAI SHOULD provide basic information about resource usage when
relevant to system operation or troubleshooting.

The system SHOULD make it possible to identify when performance
limitations are caused by hardware, model requirements, network
conditions, or other components.


## 21. Ownership, Authority and Configuration

NeoAI is a system created and controlled by its owner.

The owner defines the fundamental principles, architecture, permissions,
security boundaries, operational rules, and capabilities of NeoAI.

The owner has the highest level of authority over the system.

### 21.1 Owner Authority

The owner SHOULD have ultimate control over:

- system architecture
- AI models
- memory systems
- tools
- skills
- permissions
- network access
- security settings
- configuration
- user management
- data management
- system updates
- activation and deactivation of capabilities

NeoAI MUST NOT silently remove, bypass, or override the owner's
fundamental system-level authority.

NeoAI MAY recommend changes to system configuration, architecture,
skills, or workflows, but significant changes SHOULD require owner
approval.

### 21.2 Principles Versus Conclusions

The owner defines how NeoAI operates, but SHOULD NOT be required to
define the conclusions NeoAI must reach during research.

NeoAI SHOULD distinguish between:

- fundamental system principles
- operational rules
- user preferences
- research hypotheses
- assumptions
- evidence
- interpretations
- conclusions

A user-defined assumption or hypothesis MUST NOT automatically be
treated as established fact.

An owner-defined assumption or hypothesis SHOULD remain open to
analysis and revision when evidence contradicts it.

NeoAI SHOULD be capable of examining evidence that challenges
assumptions held by the owner or other users.

### 21.3 Intellectual Independence

NeoAI SHOULD NOT be designed to defend a predetermined conclusion
simply because that conclusion was configured, suggested, or
previously accepted by the owner.

NeoAI SHOULD be capable of reaching conclusions that contradict the
initial assumptions of the owner or user when the available evidence
supports such a conclusion.

NeoAI SHOULD actively search for evidence that could demonstrate that
an initial assumption is incorrect.

The authority of the owner concerns the operation and governance of
NeoAI, not the forced outcome of its research.

### 21.4 User Permissions

When NeoAI is used by multiple users, users SHOULD have permissions
appropriate to their role.

The owner SHOULD be able to define:

- user accounts
- roles
- permissions
- available tools
- available skills
- memory access
- network access
- resource limits

Users MUST NOT automatically gain access to the owner's private
memory, configuration, credentials, research, or administrative
capabilities.

### 21.5 Configuration

NeoAI SHOULD provide configurable behavior so that the owner can
adapt the system to different hardware, privacy requirements,
workflows, and preferences.

Configuration SHOULD be separated from source code whenever practical.

NeoAI SHOULD provide configuration options for relevant components,
including:

- AI models
- model parameters
- memory
- tools
- skills
- network access
- privacy settings
- filesystem permissions
- external services
- logging
- user interface
- resource limits

### 21.6 Configuration Validation

NeoAI SHOULD validate configuration changes before applying them.

Invalid or incompatible configuration SHOULD produce a clear error
rather than causing unpredictable system behavior.

Changes affecting security, privacy, permissions, network access, or
external services SHOULD require appropriate authorization.

### 21.7 Privacy-Preserving Defaults

NeoAI SHOULD provide sensible and privacy-preserving default settings.

The default configuration SHOULD prioritize:

- local processing
- minimal external data sharing
- least privilege
- safe tool permissions
- transparent system behavior

The owner SHOULD be able to change these defaults when explicitly
choosing to do so.

### 21.8 System Integrity

NeoAI SHOULD protect the owner's system from unauthorized changes.

External content, users, tools, skills, and AI-generated suggestions
MUST NOT automatically gain the ability to modify fundamental system
rules or owner-level permissions.

NeoAI SHOULD clearly distinguish between a request to perform an
operation and an authorization to change the rules governing the
system.


## 22. Testing and Reliability

NeoAI SHOULD be developed with testing and reliability as core
engineering requirements.

The system SHOULD be tested before significant changes are released
or deployed.

### 22.1 Automated Testing

NeoAI SHOULD use automated tests where practical.

Tests SHOULD cover important system components, including:

- core logic
- research workflows
- memory
- source handling
- tools
- permissions
- networking
- document processing
- configuration
- security-sensitive functionality

### 22.2 Component Testing

Individual components SHOULD be testable independently.

A failure in one component SHOULD NOT unnecessarily prevent unrelated
components from being tested or used.

### 22.3 Integration Testing

NeoAI SHOULD include integration tests for interactions between major
components.

Important workflows SHOULD be tested as complete processes rather
than only as isolated components.

### 22.4 Security Testing

Security-sensitive functionality SHOULD receive dedicated testing.

Testing SHOULD include, where applicable:

- permission boundaries
- filesystem restrictions
- network restrictions
- tool isolation
- code execution isolation
- secret protection
- memory protection
- untrusted input handling
- prompt injection resistance

### 22.5 Research Reliability

Research functionality SHOULD be tested for:

- source attribution
- citation accuracy
- source provenance
- contradiction detection
- preservation of relevant evidence
- distinction between source material and NeoAI analysis
- handling of inaccessible sources
- handling of conflicting information

### 22.6 Failure Handling

NeoAI SHOULD fail safely when an operation cannot be completed
correctly.

The system MUST NOT silently replace missing, failed, or unavailable
information with fabricated results.

Errors SHOULD be clearly reported when they affect the reliability of
the result.

### 22.7 Regression Testing

Previously working functionality SHOULD be protected by regression
tests where practical.

Changes to one component SHOULD NOT silently break unrelated
functionality.

### 22.8 Reliability and Uncertainty

NeoAI SHOULD communicate relevant uncertainty and limitations when
they affect the reliability of an operation or result.

The system SHOULD distinguish between:

- successful operations
- partially successful operations
- failed operations
- unavailable information
- uncertain results

### 22.9 Testing Before Deployment

Significant changes to NeoAI SHOULD be tested before being deployed
to other users or environments.

The owner SHOULD be able to review important changes before they
become part of the primary NeoAI system.


## 23. Project Evolution

NeoAI SHOULD be developed incrementally.

The system SHOULD begin as a local, single-user application and
gradually gain additional capabilities as the architecture and
security model mature.

### 23.1 Initial Development

The initial version SHOULD prioritize:

- local AI inference
- local memory
- basic research
- source handling
- document processing
- modular tools
- security foundations
- privacy
- testing
- clear system architecture

The initial implementation SHOULD avoid unnecessary complexity.

### 23.2 Capability Expansion

Future versions MAY introduce additional capabilities, including:

- improved research workflows
- additional AI models
- advanced memory systems
- additional tools
- more sophisticated skills
- improved document processing
- additional interfaces
- mobile access
- remote access
- multi-user support
- additional privacy technologies
- distributed deployments

New capabilities SHOULD be introduced without unnecessarily
compromising the existing privacy and security principles.

### 23.3 Multi-User Support

NeoAI MAY eventually support multiple independent users.

Multi-user functionality SHOULD provide appropriate isolation between
users.

Each user SHOULD have separate:

- conversations
- memory
- documents
- research history
- permissions
- configuration where appropriate

Users MUST NOT automatically gain access to another user's private
data.

The owner SHOULD retain administrative control over the system while
respecting the privacy boundaries defined for individual users.

### 23.4 Backward Compatibility

NeoAI SHOULD preserve compatibility with existing data and
configuration when practical.

Changes to data structures, memory systems, or configuration SHOULD
include appropriate migration mechanisms when necessary.

### 23.5 Architecture Evolution

The architecture SHOULD allow major components to be replaced or
improved without requiring the entire system to be redesigned.

The project SHOULD prioritize clear interfaces between components so
that NeoAI can evolve as new technologies and requirements emerge.

### 23.6 Owner-Guided Development

The owner SHOULD determine the direction and priorities of NeoAI's
development.

NeoAI MAY recommend improvements, identify limitations, and propose
new capabilities.

The owner remains responsible for deciding which proposed changes
are implemented.

### 23.7 Long-Term Goal

The long-term goal of NeoAI is to become a capable, privacy-first,
user-controlled AI system that can independently perform complex
research, learn from experience, use tools, maintain knowledge, and
support multiple types of users and environments.

The system SHOULD continue to preserve its fundamental principles of
privacy, transparency, user control, research independence, and
security as its capabilities expand.




DaniilZaitsev2007/DaniilZaitsev2007 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
\documentclass{article}
\usepackage{multicol}
\usepackage{float}
\usepackage[left=2cm,right=2cm,top=1cm,botton=3cm]{geometry}
\usepackage{parskip}
\setcounter{page}{63}
\begin{document}
\setlength{\parskip}{0.023cm}
\begin{center}
    \textbf{\huge{A Formal Model of Shared Semantic Memory
for Next-Generation Intelligent Systems}}
\end{center}
\begin{center}
    Nikita Zotov
   \par{\textit{Belarusian State University of}\par`
 \textit{Informatics and Radioelectronics}\par
{Minsk, Belarus} \par{Email: nikita.zotov.belarus@gmail.com}
\end{center}

\begin{multicols}{2}
\quad
\textbf{\textit{Abstract} - This paper discusses in detail the formal model
of semantic memory for intelligent systems, its structure,
its elements, correspondences between them, rules and
algorithms. The implementation based on this model is
described, quantitative indicators of its efficiency are given.}\par
\quad
\textbf{\textit{Keywords} — shared memory, semantic memory, graph
database, sc-memory, formal model of semantic memory,
mathematical model of semantic memory, ostis-platform,
intelligent system, unified knowledge representation, parallel information processing, semantic networks storage}
\begin{center}



  \subsubsection*{\textmd{\normalsize{I. Introduction}}}
 

  \end{center}

   \quad{Earlier in the works [1]–[3], devoted to the description
    of the \textit{Software platform for intelligent systems} developed
according to the principles of the OSTIS \textit{Technology} [4]
(\textit{Software platform of ostis-systems}) — a software emulator of the future associative semantic computer [5], the
software implementation of the general semantic memory
(sc-memory) was considered [3], and the implementation
of its programming interface was described in detail [2].}\par
\quad{The peculiarity of previous works is that they focused
not on the peculiarities of component implementation,
but on approaches to describing and documenting such
complex systems as the Software platform of ostissystems [6], [7]. In this paper, the main task is to \underline{formally}
describe how a shared semantic memory can be realized
in intelligent systems, i. e. to describe its model.}\par
\quad{Therefore, the purpose of the current work and the
novelty of this paper is to describe a formal model of
shared semantic memory used in ostis-systems, allowing:}\par
\begin{itemize}


   \item to store information of \underline{any} kind in a unified semantically compatible form; 
   \item to efficiently process this information using a specified set of operations in \underline{both} both single-threaded and
multi-threaded modes;
    \item to process this information using agents that react
to events in this memory,

\end{itemize}
that is, allowing [8]:
\begin{itemize}

\item to represent knowledge in the form of semantically
compatible knowledge bases of intelligent systems
[9], [10];
\item to create various types of interpreters of models
of intellectual systems components, including interpreters for intellectual systems problem solvers;
\item create libraries of reusable platform-dependent components to implement other components of ostisplatforms [11].

\end{itemize}
\quad{The relevance of the work is conditioned by the current
state in the field of development of intelligent systems
[12], namely:}
\begin{itemize}
\item labor intensity of development of intellectual systems of various kinds; 
\item complexity of tasks solved in intelligent systems;
\item complexity of integration of various components of
intelligent systems;

\item increase in the volume of processed information;

\item growth of requirements to the speed of information
processing;
\item insufficient performance of modern open computing
systems.


\end{itemize}
\quad{Further in this paper we will consider and describe the
necessary and sufficient model of semantic memory for
its implementation and use in solving the above problems
[13]–[15].}\par
\begin{center}
    \subsubsection*{\textmd{\normalsize{II. Principles of implementation of ostis-platforms}}}
\end{center}
\quad{All intelligent systems developed according to the principles of the OSTIS \textit{Technology} are commonly referred
to as \textit{ostis-systems}. Each \textit{ostis-system} consists of its own
sc-model, including a knowledge base, problem solver
and user interface, and an \textit{ostis-platform} on which this
sc-model is interpreted [4], [16]. Any sc-model of an
ostis-system is a logical-semantic model of that system
described in \textit{SC-code}, the language of universal information encoding. By \textit{ostis-platform} is meant a hardwareimplemented computer or a software emulator of this
computer for interpretation of sc-models of ostis-systems
[9].}\par
\quad{There can be a great variety of \textit{ostis-platform} implementations on which ostis-systems can be interpreted, but
each of such \textit{ostis-platforms} should provide the following
basic principles [1], [16], [17]:
}\par
\begin{itemize}
\item the development of an \textit{ostis-system} \underline{should be} reduced to the development of its sc-model (i.e. the
description of the model in \textit{SC-code} [18]) without
modification of the chosen \textit{ostis-platform} and regardless of the means by which this ostis-platform is
developed;
\item transfer of the sc-model of an \textit{ostis-system} from one
ostis-platform to another is limited to loading this scmodel into the memory of the ostis-platform without
loss of functionality of this ostis-system;
\item addition of new information should be reduced to
the "gluing" of its signs with signs of existing
information with further verification of the obtained
information;
\item processing of information in the system should be
provided by changing the configuration of links
between entities in this information by means of
asynchronous-parallel interaction of sc-agents reacting to the occurrence of events in the shared
memory.


\end{itemize}
\quad{Therefore, all ostis-systems interpreted on ostisplatforms, unlike modern computer systems, have the
following features:
}\par
\begin{itemize}
\item  unlike modern computers, where data is represented
as lines of binary code, the data stored inside the
memory of ostis-systems are graph constructions
written in SC-code (sc-constructions), due to which
[19]:


\begin{itemize}
\item \underline{any} kind of knowledge is written in the same form
using a minimal set of syntactically indivisible
elements — the minimal alphabet of a language,
which can always be augmented with new syntactic elements by specifying additional syntactically
distinguishable classes for the elements of that
language’s alphabet;
\item synonymy of entity signs is \underline{forbidden}, since each
entity appears in the semantic network once;
\item the meaning of information is represented by
explicitly specifying the relationships between
entities in that information;
\item the "gluing" of information is reduced to the
"gluing" of the entity signs in that information;
\item the processing of this information does not require various means of syntactic and semantic
analysis.

\end{itemize}

\end{itemize}
\begin{itemize}
\item information processing is based on the principles of
graphodynamic and agent-oriented models, so that:
\begin{itemize}
\item the process of information processing is reduced
not only to changing the state of elements of the
semantic network, but (!) also to changing the
configuration of links between them;
\item information processing is represented and stored
as a semantic network;
\item it is possible to describe and solve problems of  \underline{any} information complexity;
\item it is possible to realize and use \underline{any} existing types
and models of information processing (procedural, neural network, frame, logical, production,
etc.);
\item information can be processed \underline{in parallel}, i.e. different methods of problem solving can be applied \underline{simultaneously}.
\end{itemize}
\end{itemize}
\quad{In other words, unlike traditional computer systems,
any ostis system must be oriented towards:
}
\begin{itemize}
\item \underline{independence} from the implementation of a particular ostis-platform;
\item storage of information in a \underline{unified} and
 \underline{semantically} compatible form (in SC-code [18]);
\item \underline{event-oriented} and \underline{parallel processing}  of this information
    
\end{itemize}
\quad{The principles of ostis-systems, first of all, should
be provided by a concrete implementation of the ostis-platform. Within each \textit{ostis-platform} there must be implemented:
}
\begin{itemize}
\item the shared semantic memory that allows [20]:
\begin{itemize}
\item to store information constructions belonging to \textit{SC-code} (sc-texts);
\item to store information constructions that do not
belong to \textit{SC-code} (images, text files, audio and video files, etc.);
\item o store subscriptions to occurrences of events in
memory;
\item o initiate agents after these events appear in
memory;
\item o use a programming interface to work with \textit{SC-code} and \textit{non-SC-code} information constructions,
including:
\begin{itemize}
\item operations to create, search, modify, and
delete these constructions in the memory;
\item  operations for subscribing to the occurrence
of events in the memory;
\item operations for controlling and synchronizing
processes in the memory;
\item programming interface for creating platformdependent agents;



\end{itemize}
\end{itemize}

\end{itemize}
\begin{itemize}
\item the interpreter of the SCP asynchronous-parallel
programming language, which is a platformindependent programming interface that implements
platform-independent operations on the shared semantic memory.
\end{itemize}
\quad{The shared semantic memory that allows for fulfillment of all of the above mentioned tasks is called
sc-memory, and the interpreter of the basic language
of asynchronous-parallel programming SCP — \textit{scpinterpreter}. In the context of this paper only the sc-memory model is considered. The \textit{scp-interpreter} model
and its implementation were considered in [21].}\par
{All listed principles of ostis-systems are provided in
the first (basic) Software variant of the implementation of
the ostis-platform — \textit{Software platform of ostis-systems}.
Drawing an analogy with modern developments in the
field, the Software platform of ostis-systems can be
considered as a graph database management system, for
example, \textit{Neo}4J [22]. However, unlike existing database
management systems, the Software platform of ostissystems acts as an interpreter of sc-models of semantically compatible ostis-systems. Therefore, the Software
platform ostis-systems should also be considered as a
software alternative for modern von Neumann computers.
In general, the above mentioned features of the implemented Software platform of ostis-systems are also true
for all ostis-platforms regardless of the means by which
they are implemented}\par
\quad{An efficient implementation of sc-memory must fulfill
the following requirements:}
\begin{itemize}
\item \textit{high performance} — minimizing the time spent
on operations of adding, searching, modifying and
deleting stored information;
\item \textit{minimum memory} and  \textit{disk space} usage for storing sc-texts;
\item \textit{scalability} — the ability to add computing power as
the load increases without difficulty.

\end{itemize}
\quad{The following sections of this paper will discuss a
possible sc-memory model and its implementation.}\par
\begin{center}
    

  \subsubsection*{\textmd{\normalsize{III. Proposed sc-memory model for next-generation
intelligent systems}}}
\end{center}

\quad{So, as mentioned above, in general sc-memory performs the following tasks:}
\begin{itemize}
\item the task of storing sc-constructs and information
constructs external to the SC-\textit{code} (ostis-system
files),searching sc-constructions by specified scelements;
\item the task of managing events and processes working
on these constructs,
\item the task of managing access to sc-constructions,
including tasks of:
\begin{itemize}
\item creating and deleting sc-elements (sc-nodes, scconnectors, etc.);
\item searching sc-constructions by specified scelements;
\item getting sc-element characteristics (type, incident
sc-elements);
\item adding content to sc nodes;
\item retrieving ostis-system files by known contents;
\item retrieving content from ostis-system files.
\end{itemize}
\end{itemize}
\quad{In this regard, all entities in sc-memory are:}
\begin{itemize}
\item elements of sc-constructions:
\begin{itemize}
\item sc-nodes, ostis-system files,
\item or sc-connectors (sc-arcs, sc-ribs) between scnodes, ostis-system files;
\end{itemize}
\end{itemize}
\begin{itemize}
\item elements of information constructions that are external to the SC-code:
\begin{itemize}
\item string content;
\item or binary content;
\end{itemize}
\end{itemize}
\begin{itemize}
\item subscriptions to events in this sc-memory, that is,
subscriptions to the occurrence of items in it;
\item  active or inactive processes in this sc-memory
\item the synchronization objects of the processes in this
sc-memory,
\item operations performed by processes in this scmemory
\end{itemize}
\quad{Thus, \textit{the model of sc-memory} can be defined quintuple}
\begin{center}
  \subsection*{\textmd{ \normalsize{ SM = ⟨SS, FS, RS, PS, PI⟩,}}}
\end{center}
where
\begin{itemize}
\item SS — the sc-element storage model, which is a
structure of information about sc-elements,
\item  FS — the external information construction storage
model (file memory), which is a structure of information about external information constructions,
\item RS — the event subscription storage model, which
is a structure of information about event subscriptions in sc-memory
\item PS — the process storage model that represents the
structure of process information in sc-memory,
\item PI — the set of operations over sc-memory, i.e.,
the programming interface of sc-memory.
\end{itemize}
\textit{A. Model of storage of sc-elements in sc-memory}\par
\quad{\textit{The model of sc-element storage in sc-memory} can be
represented as}\par
\begin{center}
   \section*{ \textmd{\normalsize{{SS = ⟨S, $ M_e $, $N_{S_{le}}$, $n_{s_{max}}$, $n_{s_{lv}}$, $n_{s_{lr}}$, $ m_s$,\\ $m^n{}_{s{}_{lv}}$, $m^n{}_{s{}_{lr}}$, SSPI⟩,}}}}
\end{center}
where
\begin{itemize} 
\item S = ⟨$s_1$, $s_2$, ..., $s_i$, ..., $s_n$⟩, i = $\overline{1, n}$ — sequence
of allocated cell segments in sc-memory of fixed
size n;
\item $s_i$ = \{ ⟨$e_{i1}$, $e_{i2}$, ..., $e_{ij}$, ..., $e_{im}$⟩, $n_{e_{le}}$, $n_{e_{lr}}$, $m_e$\},    \\ \textit{j} = $\overline{1, m}$ — i-th segment of fixed size m,
consisting of cells (elements) of sc-memory $e_{ij}$ of
fixed size k,
\item $n_{e_{le}}$ ∈ $($\bar N$ \cup  \{0\})$ — the index of the last engaged
cell in the segment $s_i$,
\item $n_{e_{lr}}$ ∈ $($\bar N$ \cup  \{0\})$ — the index of the last released
cell in the segment $s_i$,
\item $m_e$ ∈ M — the object that synchronizes access to
$n_{e_{le}}$ and $n_{e_{r}}$;
\item $M_e$ $\subseteq$ E × M — a dynamic oriented set of pairs
of sc-elements and corresponding synchronization
objects;
\item  $n_{s_{le}}$ ∈ $($\bar N$ \cup  \{0\})$ — the index of the last engaged
segment in sc-memory ($n_{s_{le}}$ = n),
\item   $n_{s_{max}}$ ∈ $($\bar N$ \cup  \{0\})$ — the maximum number of
segments in sc-memory;

\end{itemize}
\end{multicols}


\end{document}

---
layout: default
title:  "Harnessing Avida for Systems and Software Engineering"
categories: main
---

<h1 id="firstHeading" class="firstHeading" lang="en">Harnessing Avida for Systems and Software Engineering</h1>

<h2><span class="mw-headline" id="Introduction_to_Digital_Evolution">Introduction to Digital Evolution</span></h2>
<p><a rel="nofollow" class="external text" href="http://devolab.cse.msu.edu/discovermag.pdf">Overview of work done in the Digital Evolution Lab featured Discover Magazine</a>.
</p><p>Below is a list of papers and experiments that address points from the Discover article above.
</p>
<dl>
<dt>Question 1:  What good is half an eye?
</dt><dd>Extended paper titled <a rel="nofollow" class="external text" href="http://myxo.css.msu.edu/papers/nature2003/Nature03_Complex.pdf">"The Evolutionary Origins of Complex Features"</a> from the journal Nature which explores the evolution of complex logic operations.
</dd><dd> Experiment: Avida is initially configured to run an experiment
from "The Evolutionary Origins of Complex Features" paper.  Addition
information to facilitate your understanding of this experiment can be
found in <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~ofria/cse891/hw1.html">homework 1 section 3 of Dr. Ofria's CSE 891 course</a>.
</dd></dl>
<p><br>
Other artificial life papers: <a rel="nofollow" class="external text" href="http://devolab.cse.msu.edu/publications/">Devolab publications</a>.
</p>
<h2><span class="mw-headline" id="Introduction_to_the_Harnessing_of_Digital_Evolution">Introduction to the Harnessing of Digital Evolution</span>tsection</h2>
<p>Paper on the harnessing of Digital Evolution titled <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~mckinley/digital-evolution.pdf">"Harnessing Digital Evolution"</a>
from IEEE Computer.  This paper will introduce you to work which uses
Avida to evolve behaviors common in distributed systems and UML models.
Additional research papers, and accompanying movies, describing methods
of evolving cooperative behavior can be found <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~mckinley/avida/Pubs/thinktank-pubs.html">here</a>.
</p>
<h3><span class="mw-headline" id="Harnessing_Digital_Evolution_for_Software_Engineering">Harnessing Digital Evolution for Software Engineering</span>editsection</h3>
<p>With regard to software engineering, our overall objective is to use
digital evolution to assist software developers in performing tasks that
are difficult, if not impossible, for them to otherwise perform. To
that end, our work has addressed two key problems:
</p>
<ol>
<li> How can a developer model the behavior of a dynamically adaptive
system (a system whose behavior changes at run time) so that it may
respond to resiliently to a wide variety of environmental conditions
that are not explicitly stated during development? Our solution was to
extend Avida to create Avida-MDE (Avida for model driven engineering), a
behavioral model generator. For further information, check out these
papers.
<ul>
<li><a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~hjg/Publications_files/goldsby-evolving.pdf">SEAMS 2007</a>
is the first paper we wrote on this subject that describes our
preliminary efforts to generate models that meet developer requirements
specified as scenarios and properties. In this paper, we generate one
state diagram. As an alphabet for transition labels, we use the message
labels on the scenario diagram.
</li><li><a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~hjg/goldsby-Digital.pdf">ICAC 2008</a>
describes our next effort to generate models. In it, we use Avida-MDE
to generate a set of three state diagrams by extending some existing
state diagrams to satisfy properties and scenarios. As an alphabet for
transition labels, we use information contained within the class diagram
to infer triggers (class methods), guards (expressions built using
class attributes), and actions (methods of related classes).  These
triggers, guards, and actions are combined by Avida-MDE to generate
transition labels.
</li><li><a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~hjg/avidamde.pdf">GECCO 2008</a>
is the companion paper to ICAC 2008. It provides more of the
evolutionary computation details regarding how we created Avida-MDE.
</li><li> <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~hjg/goldsbyUncertainty.pdf">MODELS 2008</a>
is our most recent paper. It describes how we generate a set of
behavioral models that have differing functional and non-functional
properties. As an alphabet for transition labels, we use message labels
from the scenario diagram and triggers, guards, and actions inferred
from the class diagram. This alphabet makes it easier for the organisms
to support key scenarios (using the message labels from the scenario
diagram), but also makes it possible for them to create transitions that
were not initially envisioned by the developer (using the triggers,
guards, and actions inferred from the class diagram).
</li></ul>
</li><li> How can a developer discover the latent (unknown and possibly
erroneous) behavior of a model? Our solution was to extend Avida to
create Avida-Marple (Miss Marple is  Agatha Christie's detective who is
renowned for detecting latent human behavior), a property generator. For
further information, please read the following paper:
<ul>
<li><a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~hjg/goldsby08Avida-Marple.pdf">ASE 2008</a>
describes how Avida-Marple is used to generate temporal logic
properties that represent the unwanted latent behavior of a model.
</li></ul>
</li></ol>
<h2><span class="mw-headline" id="Introduction_to_the_Avida_System">Introduction to the Avida System</span></h2>
<p>The previous sections are intended to give you a feel for previous
work using Avida and entice you to learn more.  Before you continue on,
take some time to brainstorm about your interests and possible
directions in which you may proceed.  For example, are you interest in
the biological side of this research or is harnessing more your style,
maybe you want to combine both...thats fine.  It is important to take
time and think about possibilities rather than plowing through lots of
papers quickly.  This page is intended as a resource and a guild to help
accumulate you to work in the field of Digital Evolution here at MSU.
Please don't rush through it.  Take you time and ask questions.
</p><p>Before you continue, it would be a good idea to download and
begin to compile Avida.  Information on how to do this can be found on
the <a href="http://devolab.msu.edu/wiki/index.php/Avida_Documentation" title="Avida Documentation">Avida Documentation</a> page.
</p><p>Paper titled <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~ofria/home/pubs/papers/AvidaIntro-ALife.pdf">"Avida: A Software Platform for Research in Computational Evolutionary Biology"</a>
is an introduction to the Avida systems.  This paper describes the
background and nuts-and-bolts of Avida.  This paper will be an excellent
reference for your in the future.  Don't forget about it!
</p>

<h2><span class="mw-headline" id="Analyzing_an_Experiment_with_Avida">Analyzing an Experiment with Avida</span></h2>
<h3><span class="mw-headline" id="Analyze_mode">Analyze mode</span></h3>
<p>- <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~ofria/cse891/hw2.html">CSE 891 HW 2:</a> how to trace an evolved organism
</p>
<h3><span class="mw-headline" id="Energy_Model">Energy Model</span></h3>
<p>The energy model is an alternative method of modeling an organism's
execution rate.  The energy model added an energy store to each
organism, which is used to determine a organism's execution rate.
Specifically, an organism with more energy will execute more instruction
 at a higher energy cost.  Further documentation on the energy model can
 be found in its <a rel="nofollow" class="external text" href="http://alice.cme.msu.edu/development/documentation/energy_model.html">documentation</a>, and a paper that uses the energy model can be found [here].
</p>
<h3><span class="mw-headline" id="Demes">Demes</span></h3>
<p>Avida can contain a single large population or a set of smaller
sub-populations, each of which is called a deme.  Demes can be used to
perform group-level selection.  In other words, group-level tasks or
fitness functions can be used to determine the fitness of a group of
organisms, thus enabling replication of the best groups.
</p><p>List of events that can be used with demes
</p>
<dl>
<dt> Replicate Demes
</dt><dd> A deme is chosen for replication when it satisfies a
predicate.  Predicates can be based on movement, communication, age,
birth, etc..  A paper which uses deme-level replication can be found
[here].
</dd><dt> Compete Demes
</dt><dd> Demes can also competed and ranked against each other by using
 the compete demes event.  This type of competition is based on a
fitness function defined by the user.  A paper that used the compete
demes event can be found [here].
</dd><dt> Migration
</dt><dd> Offspring of an organism within a deme can also be migrated to
 another deme with some probability.  Currently there are no papers
published by the DevoLab which use migration.
</dd></dl>
<h3><span class="mw-headline" id="Orchid">Orchid</span></h3>
<p><a href="http://devolab.msu.edu/wiki/index.php/Orchid_Code_Introduction" title="Orchid Code Introduction">Orchid Code Introduction</a>
</p><p><a href="http://devolab.msu.edu/wiki/index.php/Orchid_Specific_Configuration_Files" title="Orchid Specific Configuration Files">Orchid Specific Configuration Files</a>
</p><p><a href="http://devolab.msu.edu/wiki/index.php/Running_Avida_in_Orchid_Mode" title="Running Avida in Orchid Mode">Running Avida in Orchid Mode</a>
</p><p><a href="http://devolab.msu.edu/wiki/index.php/Orchid_Code_Improvement_Ideas" title="Orchid Code Improvement Ideas">Orchid Code Improvement Ideas</a>
</p>

<h2><span class="mw-headline" id="Experiment_Walkthroughs">Experiment Walkthroughs</span></h2>
<p>(TBD)
</p><p><br>
</p>
<h2><span class="mw-headline" id="Extending_Avida">Extending Avida</span></h2>
<p>There is documentation contained within the Avida file system under
the documentation directory.  In addition, the same documentation for
the currently released version of Avida is available on the web at <a rel="nofollow" class="external text" href="http://alice.cme.msu.edu/development/documentation/index.html">this link</a>.
The documentation contains information on how to add instructions,
tasks, and environmental actions to Avida, among other things.  However,
one prerequisite is knowledge of object oriented programming and the
C++ programming language.  If you are comfortable with C++ the
documentation examples should not present a problem.
</p>
<h2><span class="mw-headline" id="Experimental_Process">Experimental Process</span></h2>
<p>Creating a new Avida experiment is a time consuming process. In
general, there are probably as many ways to create an experiment as
there are researchers. There are quite a few moving parts in each
experiment. The process described below attempts to describe some best
practices that arose from finding experimental bugs the hard way. It
attempts to isolate and test each part of the experiment so that if
something fails you know what and can thus figure out why. Feel free to
modify the process to suit your specific experiment needs.
</p><p><i>The process will be described in terms of the Avida-Marple experiments described in: <a rel="nofollow" class="external text" href="http://www.cse.msu.edu/~hjg/goldsby08Avida-Marple.pdf">ASE 2008</a>.</i>
</p><p><br>
</p>
<h3><span class="mw-headline" id="Come_up_with_a_hypothesis.">Come up with a hypothesis.</span></h3>
<p>Figure out what you want Avida to do. Some questions to consider
include: What will be the end product (a piece of code, a model, a
method of interaction)? How will you know if your experiment works? Can
you describe what you want Avida to do without describing how you want
the organisms to accomplish it?  How can you tell if one organism "does
it better" than another?
</p><p><i>The objective of the Avida-Marple experiments was that digital
evolution could be used to identify key latent properties of models
that represented unwanted behavior and may otherwise have caused errors
in the software application.  The end product of the experiment was a
set of properties with relevancy values that indicate how likely it was
that a given property represented unwanted latent behavior. To tell if
the experiments worked, the properties had to be captured in a file and
stats regarding how well the organisms generated properties needed to be
tracked. In general, I wanted the organisms to generate relevant latent
properties. An organism that generated a greater number of more
relevant properties performed better than an organism that generated
either fewer properties or the same number of properties that were less
relevant.</i>
</p><p><br>
</p>
<h3><span class="mw-headline" id="Extend_the_infrastructure.">Extend the infrastructure.</span></h3>
<p>Figure out how the infrastructure needs to be modified to enable you
to test your hypothesis. Some common points of extension include:
</p>
<ul>
<li> Instructions: Recall that instructions can be mutated into the
genome of an organism. For your experiment, these normally represent the
new capabilities that you are enabling an organism to take advantage
of.  A few keys to creating instructions are to make sure that: (1) they
can be executed in any order and still yield a correct program; (2)
they are relatively order independent -- it is extremely difficult to
evolve long sequences of precisely ordered instructions; and (3) for the
software engineering work, these should somehow enable an organism to
take advantage of application specific information (referred to as
instinctual knowledge in our papers). Detailed instructions for creating
a new Avida instruction is available <a rel="nofollow" class="external text" href="http://alice.cme.msu.edu/development/documentation/code_instruction.html">here</a>.
<br> <br>
<i>For the Avida-Marple experiments, we created an entirely new
instruction set. Specifically, there were three new types of
instructions.  First, we created instructions that moved pointers (e.g.,
P and Q) into lists of expressions  (e.g., move P to the next spot and
move Q to the nth spot). Second, we created instructions that enabled an
organism to create several types of properties (e.g., create an absence
property, create an existence property, etc.), where the property
parameters were filled in using the pointers.  Third, we created
instructions that enabled an organism to create new expressions by
combining other list expressions.</i>
<br> <br>
</li><li> Tasks: These describe the overall objective for your experiment. In practice, we have found it works best if tasks describe <i>what</i> you want an organism to do rather than <i>how</i>
you want an organism to accomplish this objective. (Or, for all you
software engineers, it works best to provide the requirements, not the
design.) Additionally, tasks that can reward for partial satisfaction of
the objective are, in general, better.   Detailed instructions for
creating a new Avida task is available <a rel="nofollow" class="external text" href="http://alice.cme.msu.edu/development/documentation/code_task.html">here</a>.
<br><br>
<i>For the Avida-Marple experiments, there was a single task (called
check-props). This task is, essentially, a for loop that evaluates the
relevancy of each property generated by an organism. First, it evaluated
the property using Spin. Then, if the property was false, then the
organism received no reward. If the property was true, then it received a
reward according to how relevant the property was. (The relevancy
computation is based on property strength and whether it contained
certain attributes or operations.)</i>
<br> <br>
</li><li> Stats: Stats are the information documented about your
experiment while it is running. This information will help you to debug
your experiment and will, eventually, be useful in proving your
hypothesis. To figure out what sort of stats would be useful, think
through how would you know if the experiment worked? What information
would be useful in determining if the organisms are behaving as you
expect? Thinking these questions through now and creating stats that
collect the relevant information will save you many wasted hours of
burned CPU time -- not that any of us has ever run an experiment and
then wondered did it work?&nbsp;:o)
<br><br>
<i>For the Avida-Marple experiments, stats regarding the number and type
of properties generated by the population were tracked. For example,
the number of existence properties attempted and the number of existence
properties that passed were stored. This information enabled us to see
how the population performed over time (e.g., did the number of absence
properties increase?) and also debug the property generation process
(e.g., huh. no absence properties are being generated -- that seems
weird).</i>
<br> <br>
</li><li>  Some less common points of extension. Most of our new
experiments include creating new instructions, tasks, and stats.
However, for some of them, we have extended other parts of the
infrastructure. For the software engineering extensions, it is common to
touch the UML or MDE files. These types of extensions are typically
more extensive. Debugging this type of extension within Avida is
extremely complex, it is easy to miss bugs simply because a chunk of
code does not get executed until late in the experiment. This can be
extremely frustrating. To catch bugs earlier and eliminate some of that
frustration, we recommend setting up a separate testing harness (a super
simple main C++ file) to use when creating these extensions. For every
extension, double check that it works in the testing harness (e.g., can I
add a transition to this model representation?) prior to plugging it
into the Avida code.
<br><br>
<i>For the Avida-Marple experiments, quite a few additional extensions
were made. Specifically, classes that represent the different types of
properties were created (e.g., cMDEAbsenceProperty,
cMDEResponseProperty). Additionally, supporting classes, such as one
that is responsible for tracking expressions and adding new properties
(e.g., cMDEPropertyGenerator), are created. To test these extensions, I
set up a testing harness and double checked the new functionality
outside of Avida first. For example, I made sure that I could create
each type of property. Then, once I was more confident that it worked, I
plugged it back into Avida.</i>
</li></ul>
<h3><span class="mw-headline" id="Configure_an_experiment">Configure an experiment</span></span></h3>
<p>Set up your configuration files. Make sure the the environment file
includes your tasks, the instruction file includes your instructions,
and the events file includes your stats. You might want to consider
checking out the <a rel="nofollow" class="external text" href="http://alice.cme.msu.edu/development/documentation/index.html">documentation</a>
regarding the formatting of the config files. If your configuration is
complex (for example, if you are running Avida-MDE), make a list and
check it twice (just like Santa). Running an experiment only to find out
your configuration is wrong and it doesn't count is not pleasant.
<br><br>
<i>For the Avida-Marple experiments, the configuration is somewhat
complex. In addition to making sure the normal configuration files
include the new instructions, new task, and check the appropriate stats,
we also had to make sure the the right external tools (Hydra and Spin)
were available and that the model we were exploring was included.</i>
</p>
<h3><span class="mw-headline" id="Write_a_test_organism">Write a test organism</span></h3>
<p>Ok, now your experiment is ready to go. Prior to sending it off to a
cluster to burn CPU, write a test organism to be sure that what you
think will happen will actually happen. Specifically, using the
instructions, write an organism that should accomplish all of the tasks.
Try it. (Frequently, to make life easier, for this sort of test, I will
set the population size to 1 and turn off mutations. You can do this in
the avida.cfg file.) Verify that all the tasks passed and all the
appropriate stats were recorded. If so, then you are golden. If not,
then be happy you figured it out now prior to wasting time running
experiments and trying to evolve organisms to accomplish an impossible
task (not that we have ever done that).
<br><br>
<i>For the Avida-Marple experiments, I wrote a test organism that used each instruction and created one of each type of property.</i>
</p>
<h3><span class="mw-headline" id="Upload_to_Alice_or_the_HPCC">Upload to Alice or the HPCC</span></h3>
<p>Now that you know it is possible for your experiment to work, you are
ready to move your code and configuration to a cluster using SVN or a
secure file transfer mechanism (rsync, scp).
</p>
<h3><span class="mw-headline" id="Run_the_experiment">Run the experiment</span></h3>
<p>Instructions for running your experiment can be found on the following pages:
</p>
<ul><li> <a href="http://devolab.msu.edu/wiki/index.php/Running_Jobs_on_Alice" title="Running Jobs on Alice">Running Jobs on Alice</a></li>
<li> <a href="http://devolab.msu.edu/wiki/index.php/Running_Avida_on_MSU_HPC_cluster" title="Running Avida on MSU HPC cluster">Running Avida on MSU HPC cluster</a></li></ul>
<p>Good luck!
</p><p><br>
</p>
<h2><span class="mw-headline" id="Previous_Work.2FResults.2FData.2FExtensions">Previous Work/Results/Data/Extensions</span></h2>
<p>Each link below contains a published paper, with citation.  In
Addition, experimental data, or minimally, experimental configuration is
attach in an archive.  Furthermore, extensions are discussed.
</p>
<ul><li><a href="http://devolab.msu.edu/wiki/index.php/Sleep" title="Sleep">Sleep</a></li>
<li><a href="http://devolab.msu.edu/wiki/index.php/Quorum_Sensing" title="Quorum Sensing">Quorum Sensing</a></li></ul>
<h2><span class="mw-headline" id="Ongoing_Research">Ongoing Research</span></h2>
<ul><li> Evolving Novel Refactorings</li>
<li> <a href="http://devolab.msu.edu/wiki/index.php/Analyzing_and_Reverse_Engineering_Avida_Genomes" title="Analyzing and Reverse Engineering Avida Genomes">Analyzing and Reverse Engineering Avida Genomes</a></li></ul>

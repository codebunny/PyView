PyView
======

<h1>1. Experiment Framework</h1>

<h2>Intervals</h2>
<p> Intervals are blocks of time during the experiment. The type of interval determines the types of actions that may occur in that time. Types of interval include: </p>
	<ul>
	<li><b>Wait</b> During a wait nothing happens. No lever press are rewarded or tone delievered. Ex: ITI</li>
	<li><b>Tone</b> A tone is played throughout the duration of this interval. At the start of this interval the associated valves are also opened.</li>
	<li><b>Reward</b> If a lever is pressed during this interval, one of the active valves will deliver water.</li>
	<li><b>No Go</b> At the end of this interval a reward is given, only if the lever was never pressed during this interval </li>
	</ul>
<p>Each interval consist of the following properties:</p>
<ul>
	<li><b>Start Time</b> measured in seconds</li>
	<li><b>Duration</b> is how long the interval will take (measured in seconds). A duration may vary by a random scalor factor.</li> 
	<li><b>Action</b> links to an associated action, if there is desire to associate with action. Depending on the action mode, this action may be performed, at the start of the interval,</li>
	at the end of the interval, or anytime during the interval if a lever is pressed.
</ul>

<h2>Actions</h2>


<h1>2. Stony Brook Neurology Lab Implementation</h1>
<h2>Library packages</h2>
<ul>
	<li><b>framework</b> contains abstract experiment paradigm structure. See Experiment Framework for more info.</li>
	<li><b>libnidaqmx</b> National Intruments card driver library. Made by <a href="https://code.google.com/p/pylibnidaqmx/">Pearu Peterson</a></li>
	
</ul>
<h2>Files</h2>
<ul>
	<li><b>CondTree</b> module used to build and maintain the conditions tree used in several parts of the Editor</li>
	<li><b>Editor</b> is the graphical user interface (GUI) used to create and edit the XML experiment paradigm files</li>
	<li><b>gui</b> module containing the sub panels in PyView</li>
	<li><b>neuroconnect</b>module where all the hardware (NI card) control functions reside</li>
	<li><b>PyView</b> main experiment execution program</li>
	<li><b>test_tone</b>test tone scripts (command line)</li>
	<li><b>ToneControl</b>test tone script (GUI)</li>
	<li><b>uservars</b> list of global variables and functions. Most of them deal with the names and colors of things</li>
	
</ul>
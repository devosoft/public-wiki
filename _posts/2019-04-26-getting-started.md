---
layout: default
title:  "Getting Started in the Devolab"
categories: main
---

Welcome to the Devolab!


# Lab Infrastructure Checklist
Here's a list of the things that need to be done for a new member to be able to make use of the full lab infrastructure. Brian Baer will be able to help you with most of these:

- Get keys
- Get your MSU ID authorized to access BEACON (see Connie)
- Get your e-mail added to [Devolab mailing list](http://lists.idyll.org/admin/devolab)
- Get registered with Slack
- Get access to devolab Google calendar
- Create wiki account - have admin user go to Special:CreateAccount
- Add your information to the Member Information section of the private wiki
- Add your listing the the Devolab public web page ([devolab.msu.edu](https://devolab.msu.edu))
- Have a faculty member request an account for you on the [HPCC](http://www.icer.msu.edu/?q=hpcc)
- Have Matt or Charles put in an HPCC request to add you to the devolab and beacon groups on the HPCC
- Add user to rodan
- If you are not a CSE student -- get a CSE or EGR account if necessary
- Get added to your PI's group on the BEACON page
- If you want to be a part of Avida development, get added on the [Avida Development mailing list](http://avida.devosoft.org/mailman/listinfo/avida-dev/).
- Add to Avida Dropbox
- Have Matt create an account for you on the Alice cluster:

~~~ shell
adduser -c "full user name" -s /bin/tcsh user_name
passwd user_name
su "user_name"
ssh-keygen -t dsa
cp ~/.ssh/id_dsa.pub ~/.ssh/authorized_keys2
chmod 600 ~/.ssh/authorized_keys2
Add /usr/local/dist_run/bin to $PATH for user
exit
/usr/local/dist_run/sbin/dist_update_node_configs
~~~

# Avida

Most research in Devolab uses the Avida software.
The following articles provide a good introduction to Avida:

* [Testing Darwin](http://www.carlzimmer.com/articles/2005.php?subaction=showfull&id=1177184710&archive=&start_from=&ucat=8&) by Carl Zimmer (Cover story of Feb 2005 Discover Magazine).
* [Twice as Natural](http://myxo.css.msu.edu/lenski/pdf/2001,%20Nature,%20Lenski,%20twice%20as%20natural.pdf) by Richard Lenski (2001)
* [Meet the Scientist](http://www.microbeworld.org/index.php?option=com_content&view=article&id=784:mts59-charles-ofria-&catid=37:meet-the-scientist&Itemid=155) podcast interview of Charles Ofria by Carl Zimmer (2010)

For more detailed materials, see:

* [Avida: A Software Platform for Research in Computational Evolutionary Biology](http://www.cse.msu.edu/~ofria/pubs/2009AvidaIntro.pdf) by C. Ofria, D.M. Bryson, and C. Wilke (2009).
* The current [Avida Documentation](http://avida.devosoft.org/documentation/current/).
* Instructions for [Obtaining](http://devolab.msu.edu/wiki/index.php/Obtaining_Avida), [Compiling](http://devolab.msu.edu/wiki/index.php/Compiling_Avida), and [Running](http://devolab.msu.edu/wiki/index.php/Running_Avida) Avida.

For information on development using Avida, see:

* The Avida [Development Website](http://avida.devosoft.org/)
* Wiki notes on Avida Development
* Consistency tests in Avida should be run before you check in code (and will be run automatically afterward).
  These tests ensure that features in Avida are not accidentally broken during unrelated code changes.
  When you add a new feature, make sure to [setup a new test](http://devolab.msu.edu/wiki/index.php/Setup_a_New_Test).

If you get stuck while performing research with Avida, make sure to take a look at the [Avida Research FAQ](http://devolab.msu.edu/wiki/index.php/Avida_Research_FAQ).

# Software

* Dropbox is a useful file-sharing system.
  If you do not have a Dropbox account, please ask another lab member to invite you as this will give them extra space.
  Also, sign up via https://www.dropbox.com/edu, which will give you extra space.
* Wunderlist is free TODO list management software that allows multiple people to share lists and is helpful for project management.
* LaTeX - A document preparation language, often used for writing manuscripts.
  Overleaf is a website for collaboratively writing LaTeX papers.

# Computational Skills

* Unix shell to navigate a terminal ([Tutorial by The Hacker Within](http://hackerwithin.org/thw/plugin_wiki/page/msu_the_shell))
* A text editor to modify text files from a terminal.
  Emacs and Vim are the most popular.
  (An [overview](http://hackerwithin.org/thw/plugin_wiki/page/msu_text_editors) of some options, by the Hacker Within)
* Shell scripting to automate tasks ([Some useful notes](http://www.dartmouth.edu/~rc/classes/ksh/print_pages.shtml) from a class at Dartmouth.)
* The two languages used most in the lab are C++ and Python
* Notes from an [MSU Bootcamp](http://hackerwithin.org/thw/plugin_wiki/page/MSU2011Bootcamp) run by the Hacker Within.
* [Google University](http://code.google.com/edu/courses.html) courses.

# Scientific Methodologies and Statistical Skills

* Be sure you are comfortable with [Strong Inference](http://en.wikipedia.org/wiki/Strong_inference) techniques for scientific inquiry.
* Make sure you understand the difference between [parametric](http://en.wikipedia.org/wiki/Parametric_statistics) and [non-parametric](http://en.wikipedia.org/wiki/Non-parametric_statistics) stats.
  Most (but not all) of what we do in the lab is non-parametric.
* [Guide to choosing a statistical test.](http://www.graphpad.com/www/Book/Choose.htm)
* A selection of [visualization methods](http://www.visual-literacy.org/periodic_table/periodic_table.html).
* Remember that a [p-value](http://en.wikipedia.org/wiki/P-value) only tells you how likely that there is a difference between two difference, but nothing about the magnitude of that difference. [Confidence intervals](http://en.wikipedia.org/wiki/Confidence_interval) can help show that difference.
* Be careful when performing multiple comparisons with the same data.
  Often the safest thing to do is to redo all of your runs once you have found what you believe to be a significant result.

# Devolab Infrastructure

* DevoWiki (this wiki)
* Devolab mailing list

# Evolutionary Biology
Books to read for broad concepts:

* Darwin's Dangerous Idea by Daniel Dennett provides an excellent overview to evolutionary biology, put in a broad context and accessible to a general audience.
  Another good choice is Dawkin's The Blind Watchmaker.
* The Tangled Bank by Carl Zimmer is an accessible introductory textbook to evolutionary biology.
* Climbing Mount Improbable by Richard Dawkins describes how seemingly unlikely events (such as new complex traits) occur in the evolutionary process.
* Major Transitions in Evolution by John Maynard Smith and Eörs Szathmáry is a classic book describing large evolutionary events. See also The Major Transitions in Evolution Revisited by Brett Calcott and Kim Sterelny.
* Emergence: The Connected Lives of Ants, Brains, Cities, and Software by Stephen Johnson talks about the evolution of cooperative behaviors.
* The Making of the Fittest by Sean Carroll discusses evolution at the level of genes in a highly accessible manner.

Some papers to read:

* [Evolution and Tinkering](http://adi-38.bio.ib.usp.br/ibi5023/2010/Jacob_1977.pdf) by Jacob

# Other Background Topics

* Artificial Life
* Evolutionary Computation (Genetic Algorithms, Genetic Programming, etc.)
* Information Theory

# Important Skills for Scientists

* BUGS in Writing by Lyn Dupre gives a list of extremely useful rules for writing papers as a computer scientist.
* The Craft of Research by Booth et al. is targeted at grad students learning how to pursue a research project.
* Marketing for Scientists teaches how to setup your own brand and get your work well known.

# Internal Resources

* BEACON Center web site.
  Make sure you have an account on the intranet.
* Schedule for [BEACON Seminar Room](https://www.google.com/calendar/hosted/msu.edu/embed?src=msu.edu_pke71q0u1fu6ra64api1v8f7l8@group.calendar.google.com&ctz=America/New_York&gsessionid=OK&AuthEventSource=SSO)
* Schedule for [BEACON Conference Room](https://www.google.com/calendar/hosted/msu.edu/embed?src=msu.edu_tg51lskg3gi8bejrlthr2k5bu8@group.calendar.google.com&ctz=America/New_York&AuthEventSource=SSO&gsessionid=-paBIJTwtyEAyL1KK2Dhcw)
* List of [Graduate Student Fellowships](https://spreadsheets.google.com/ccc?key=0ApCsMjfqjcaFdEw5NnVpTm41NEFmb1lQdlROdF9teWc&hl=en&authkey=CJ-1mfYM#gid=0)

# Other External Resources

* Google Scholar - search publications.
* [Digital Evolution Yahoo group.](http://tech.groups.yahoo.com/group/DigitalEvolution/)
* [Tomorrow's professor mailing list.](http://cgi.stanford.edu/~dept-ctl/tomprof/postings.php)
* [Google Code University courses.](http://code.google.com/edu/courses.html)
* [Information Theory guide.](http://www.cs.toronto.edu/~mackay/itprnn/ps/)

# New to Michigan State University?
* CATA is our local bus service.
  It provides service for MSU, East Lansing, Lansing, Okemos, and Haslett areas.
* If you need transportation to the Detroit Metropolitan Airport you might consider using the Michigan Flyer.
* MSU is also near the East Lansing Amtrak and Greyhound station.
  We also have Megabus service.
* Useful nearby food includes:
  * Sparty's (right outside BEACON),
  * The Dairy Store (across Farm Lane; free tomato soup with Grilled Cheese on Mondays),
  * the International Center (across from the Engineering building).
* And of course, BEACON often has food at events and leftovers in the kitchen.
* You are free to use the BEACON/ICER refrigerator, but be aware that it is sometimes cleaned out -- so label anything you'll be leaving there for more than a day.
* Grand River Avenue (street directly north of campus) is filled with a variety of restaurants... favorites include
  * Jimmy Johns,
  * Five Guys,
  * Cosi,
  * Potbellys, and
  * Gumby's.
* Hannah Plaza on Hagadorn (street directly east of campus) also has various restaurants
  * Sansu (sushi),
  * Pizza House,
  * Menna's Joint,
  * Jimmy Johns,
  * Sultans (Mediterranean), and
  * Sindhu (Indian).
* Other favorites:
  * Taste of Thai,
  * Ding Tea, and
  * East Cafe.
* Make sure to register your bike before parking it outside or it will be removed.
  You can also bring your bike inside BEACON.
* There are two malls near East Lansing: Meridian Mall and Eastwood Towne Center.
  Eastwood Towne Center is an outdoors mall.
* There are two movie theaters near East Lansing: NCG in Eastwood and Celebration Cinema.
* If you are a new student or employee, you might consider opening an account at Michigan State University Federal Credit Union (MSUFCU).
  You'll find MSUFCU ATMs throughout campus and at most Quality Dairy convenience stores throughout town.
* Michiganders say some weird things and use their hands as maps.
  You can read more about Michigan's idiosyncrasies at Michigan Native.
* If you are being paid via fellowship, you usually need to pay quarterly estimated taxes, because MSU does not withhold them from your pay.
* Heads up: East Lansing and Lansing assess an income tax!
* An East Lansing ordinance prohibits parking on residential streets between 2am and 6am.
  However, if you call the non-emergency police line at (517) 351-4220 you can request overnight parking and avoid a ticket!
* Your labmates are friendly people.
  You should feel free to ask them questions as you get settled in.

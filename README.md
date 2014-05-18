SpiderAjax
---

This is a module being developed as a part of Google Summer of Code 2014 project for OWASP OWTF.



What is OWTF?
---

OWTF is a project aligned to standards such as the OWASP Testing Guide and the Penetration Testing Execution Standard (PTES). 

The main focus of OWASP OWTF is to automate the manual, uncreative part of penetration testing. OWTF tries to unite tools and expedite pentesting through automation, efficient reporting, efficient human analysis, a fast MiTM proxy, and multi-processing.


About
---

SpiderAjax is a minimalistic port of [Crawljax](http://www.github.com/crawljax/crawljax.git). 

It enables "crawling" of AJAX targets to probe for further vulnerability testing.

Essentially, the tool is divided into 4 main parts:


* <b>Clickbot</b>


This is the main spider/crawler. It fetches the base URL (uses Selenium), passes on the DOM tree to the DOM analyzer.
It also performs clicking, firing/triggering of events on certain candidate elements.


* <b>DOM Analyzer</b>

This uses the HTML source to perform parsing.

  - Compares DOM states before and after an event is triggered by the bot.

  - Calculates the difference between two states

  - Parses the new DOM state for new links, changes

  - (To be added later)


* <b>Controller</b>

This manages the clickbot and the state-flow graph engine.

It initializes, pauses, and stops the bot. This also creates the state flow graph based on DOM state changes (from the DOM analyzer).


* <b>State-flow graph</b>

This interprets visually, how the state changes with trigger/firing of an event.

An example of a state flow graph:
<hr>
![](http://crawljax.com/images/new-overview-plugin.png)

The state-flow graph can be accessed through the webUI.



Milestone
---
0.1



Contribute
---

Send a pull request or create an issue on the issue tracker.
Suggestions welcome!w
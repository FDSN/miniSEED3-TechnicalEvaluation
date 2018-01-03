# Technical Evaluation for the next generation of MiniSEED

This GitHub repository, and especially its issues, will be used for stage 2 of the design of the next generation MiniSEED format. The three stages of its design are:

* **Stage 1**: Community agreement on the actual basic requirements for the next generation MiniSEED.
* **Stage 2**: Technical evaluation of these requirements.
* **Stage 3**: Technical discussion targeting selection of the best solution.

**The goal of stage 2 is to evaluate the technical feasibility of the requirements agreed on in stage 1 and vote on which requirement are feasible and will be included in the new format. Multiple possible technical solutions for some requirements are expected and will be sorted out in stage 3.**

References to discussions and so far produced documents:

* **Mailing List Thread:** http://www.fdsn.org/message-center/thread/514/
* **Google Doc with the results from Stage 1:** https://docs.google.com/document/d/1ymAe9v1rUuucpY7ai5ilKsD7V1ejwt6GxQQmJ5IevDI


### Procedure and Timeline

1. Discussion will start right now and will be moderated by [@krischer](https://github.com/krischer/). Anyone is invited to join. A separate issue is available for each discussion point.

2. **Voting on each issue is expected to start January 29th and end January 31st** (earlier votes will of course be counted). They will be tallied up by [@krischer](https://github.com/krischer/) on February 1st. Please register to vote in [#1](/../../issues/1). You can vote either by reacting with :+1: (YES) or :-1: (NO) to the head post in an issue or by explicitly stating your support for/contra in a comment in an issue. A transparent vote summary for each issue (including names) will be provided by [@krischer](https://github.com/krischer/) after voting has concluded. [@krischer](https://github.com/krischer/) will not vote but break a tie, if necessary.

## Technical Evaluation

The discussion will be broken up in a number of issues:

### Administrative Issues:

* **[#1](/../../issues/1):** Register to vote by posting to this issue. It will also be used to flesh out who has the right to vote, if necessary.
* **[#2](/../../issues/2):** Discuss anything related to this readme here.
* **[#3](/../../issues/3):** Misc discussions. Please don't open arbitrary new issues but discuss generic things here. A new issue will be opened in case it is deemed necessary.

### Basic Requirements:

* **[#4](/../../issues/4):** A new method of identifying a time series.
* **[#5](/../../issues/5):** The new format must be fully self-defining.
* **[#6](/../../issues/6):** Specify absolute time, including leap seconds, using an existing standard.
* **[#7](/../../issues/7):** Conversion tools must perform conversion from MiniSEED 2 *without* loss of important information.
* **[#8](/../../issues/8):** Joint evolution of StationXML.
* **[#9](/../../issues/9):** Proper documentation, best practices.

### Additional Requirements:

* **[#10](/../../issues/10):** Identification of non-raw, derived data.
* **[#11](/../../issues/11):** New data payload encoding types (general, opaque).
* **[#12](/../../issues/12):** Include a CRC (cyclic redundancy check) of the complete record.
* **[#13](/../../issues/13):** Include both a format and a data/publication version number.
* **[#14](/../../issues/14):** Allow addition of arbitrary headers by equipment manufacturers, operators, etc. without the need for authorization or approval by the FDSN.
* **[#15](/../../issues/15):** Support variable length records for efficiency and flexibility (e.g. real time streaming with lower latency).
* **[#16](/../../issues/16):** Provide nanosecond-timing resolution in both record start time and sample rate/period.
* **[#17](/../../issues/17):** Provide support for high sampling rates.
* Simplification/reorganization of MiniSEED:
	* **[#18](/../../issues/18):** Move key, selected blockette details (e.g. actual sample rate, data payload encoding) into fixed header.
	* **[#19](/../../issues/19):** Fix byte order (e.g. little endian) of binary portions of header; define byte order of payload via encoding values.
	* **[#20](/../../issues/20):** Remove blockette support.
	* **[#21](/../../issues/21):** Simplify and improve record start time.
	* **[#22](/../../issues/22):** Eliminate time correction field as a required, always-present field and retain as an optional field present when needed.
	* **[#23](/../../issues/23):** Combine and drop unused / underspecified bit flags.
	* **[#24](/../../issues/24):** Eliminate sequence number as a required, always-present field and retain as an optional field present when needed.
* **[#25](/../../issues/25):** Alongside with the new format, a protocol for (near) real time data exchange needs to be specified.

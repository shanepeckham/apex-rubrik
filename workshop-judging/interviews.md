---
title: Kaiju Response Stakeholder Interview Transcripts
description: Fictional stakeholder interviews for a facilitated Scope Conversations workshop using the Apex Dynamics Response Systems scenario
ms.date: 2026-09-12
ms.topic: concept
---

## Participant Brief

Apex Dynamics has been asked to turn its attractive command-center prototype into a production system for the Pacific Kaiju Early Warning Network. The prototype combines sensor observations, a kaiju registry, a signal feed, a command map, threat levels, citywide alerts, and finite response assets.

Your team has received four interview transcripts from people involved in regional response operations. Read their statements as stakeholder perspectives, not as agreed requirements. Look for evidence of goals, pain points, constraints, disagreements, assumptions, and unanswered questions.

> [!CAUTION]
> These interviews and the people in them are fictional workshop materials. They do not represent validated user research. Validate any resulting assumptions with real stakeholders before using them for product decisions.

## Interview 1: Regional Response Dispatcher

**Participant:** Maria Chen, senior dispatcher at the Puget Sound Regional Response Center

**Context:** Maria works twelve-hour rotating shifts. During an active event, she coordinates military, emergency services, evacuation teams, and infrastructure crews while monitoring several radio channels and agency systems.

**Interviewer:** Walk me through what happens when the first unusual signal arrives.

**Maria:** Usually it does not arrive as one clean alert. Sonar reports an underwater contact. A few minutes later, the coastal array reports a wake. Then somebody from a ferry calls the civil defense line. Each source uses different language and sometimes a different sector name. My first job is figuring out whether three reports describe one kaiju or three separate problems.

**Interviewer:** What do you use to make that judgment?

**Maria:** Right now, I have the signal feed, the map, two radio consoles, a shared spreadsheet, and a paper board showing which units are available. The prototype puts more of that in one place, which is promising. But a dot on a map can look more certain than the underlying information really is. I need to know whether the location came from fresh sonar, an analyst estimate, or a civilian report from ten minutes ago.

**Interviewer:** What makes the work difficult during an attack?

**Maria:** The information changes faster than the coordination process. A unit shown as available may already be helping another region. A bridge marked open may have been closed by local police. If Nyxmora disrupts communications, the dashboard might stop updating while everyone assumes it is still live. I cannot wait for perfect data, but I need to know what is stale.

**Interviewer:** How do you decide which response asset to send?

**Maria:** I look at the target, the kaiju's behavior, travel time, civilian exposure, and what we need to hold in reserve. Jets are fast, but they are not always useful against a submerged threat. Barriers take time to charge. Evacuation teams cannot be treated like tokens. Their capacity depends on roads, buses, shelters, and whether the public follows instructions.

**Interviewer:** The prototype lets you select a kaiju and deploy an asset. How would that fit your work?

**Maria:** Selecting a target first makes sense, but it also worries me. Under pressure, someone could think Gorathos is selected when the focus has moved to Vespyra. I want a final confirmation that says what is going where and why. For a routine repositioning, I should not have to wait for the incident commander. For a citywide evacuation or use of heavy military assets, I expect an approval step.

**Interviewer:** What happens after you send something?

**Maria:** A button changing from six jets to five is not enough. I need to know whether the order was received, acknowledged, launched, diverted, completed, or failed. If the network is down, I may issue the order by radio. When connectivity returns, the system cannot send it a second time or pretend the radio order never happened.

**Interviewer:** How do citywide alerts work today?

**Maria:** The incident commander normally authorizes them, but the dispatcher may have to act if landfall is imminent and the commander is unreachable. That exception has to be visible and reviewable. The current process is slow because we repeat the alert wording, affected sectors, and expiration time across several systems. A false alarm carries a cost, but a late warning costs more.

**Interviewer:** What would make the new system successful for you?

**Maria:** I should be able to understand the current situation in seconds, see what changed, and coordinate without copying the same information into four places. I do not want the system to make the decision for me. I want it to stop hiding the operational details I need to make the decision safely.

## Interview 2: Early Warning Data Analyst

**Participant:** Dr. Owen Brooks, senior data analyst for the Pacific Kaiju Early Warning Network

**Context:** Owen monitors observations from sea, land, air, space, and civilian infrastructure. Analysts compare new tracks with the kaiju registry and brief the response center on identity, behavior, and projected landfall.

**Interviewer:** What does an analyst do when a possible kaiju is detected?

**Owen:** We start with attribution. Is this a known kaiju, a new one, or noise? A fast surface track might resemble Vespyra, while a submerged contact could match Nyxmora or Skarnyx. Height, mass, speed, movement pattern, thermal behavior, and electronic interference all help, but no source gives us every trait.

**Interviewer:** Why not let the system pick the closest registry match?

**Owen:** It can suggest candidates, but the word "match" is dangerous. Two sensors may be reporting the same event with different timestamps. A damaged sensor can be precise and wrong. A civilian video may be current but mislocated. If the interface labels a contact "Nyxmora" too early, every later observation gets interpreted through that assumption.

**Interviewer:** What would you want to see in a unified experience?

**Owen:** The combined picture, plus the path back to the evidence. Show me which observations support an identity, which contradict it, when each source last reported, and whether time or location was estimated. Confidence should not be one unexplained percentage. I need to understand why it changed.

**Interviewer:** How do you communicate uncertainty to operations staff?

**Owen:** Carefully. If I explain every caveat during an emergency, nobody can act. If I hide the caveats, they may act on a false certainty. I usually give the leading assessment, the most dangerous plausible alternative, and what evidence would change my mind. For example: "Likely Skarnyx, but Nyxmora remains possible; expect sensor disruption if the second identification is correct."

**Interviewer:** What problems occur when data volume rises?

**Owen:** Duplicate reports become a major issue. One thermal bloom can generate a drone alert, a satellite alert, and fifty public posts. Volume looks like corroboration even when all reports trace back to the same event. We also lose context when the feed keeps only the newest items. During review, I need the complete sequence, including corrections and retractions.

**Interviewer:** Would automatic threat levels help?

**Owen:** As a summary, yes. As the truth, no. The highest threat is not always the most urgent problem. Gorathos might have the highest severity class but be moving slowly toward an evacuated industrial shoreline. Vespyra might be lower class, moving quickly toward a hospital corridor. The system should expose how threat condition was derived and let us flag exceptional context without rewriting source data.

**Interviewer:** What mistakes are hardest to recover from?

**Owen:** Merging two contacts that later separate, or splitting one contact into two and dispatching twice. Silent corrections are also bad. If an analyst changes an estimated landfall from Seattle to Bellevue, everyone who acted on the earlier estimate needs to see that the assessment changed, not merely see a marker jump on the map.

**Interviewer:** What would success look like?

**Owen:** Analysts would spend less time cleaning and reconciling formats and more time evaluating evidence. Operations staff would see concise assessments without losing provenance. Most importantly, the system would make uncertainty usable instead of either burying it or flooding the room with caveats.

## Interview 3: Early Warning Network Software Engineer

**Participant:** Priya Nair, software engineer on the Pacific Kaiju Early Warning Network integration team

**Context:** Priya's team connects sensor providers and regional response centers. They support systems operated by two countries, several agencies, private infrastructure operators, and vendors with different maintenance schedules.

**Interviewer:** What concerns you about turning the prototype into production software?

**Priya:** The prototype assumes the data is already clean, current, and shaped correctly. Production starts before that point. Some sensors stream every second. Others upload a batch when a satellite link returns. Older systems send coordinates in different formats. Agency clocks drift. A message may arrive twice, late, or out of order.

**Interviewer:** Can the application normalize those differences?

**Priya:** Yes, but normalization must not erase the original observation. We need a common model for the operational view and a preserved source record for investigation. Every transformed value should be traceable to where it came from. If a conversion changes a coordinate or unit incorrectly, we must be able to find the affected assessments.

**Interviewer:** What happens during a network disruption?

**Priya:** The regional center must continue operating. The screen should distinguish "no threat detected" from "no recent data received." Those are completely different conditions. Local actions may need to be queued while disconnected, but replaying them later is risky. A deployment command must not execute twice because an acknowledgment was lost.

**Interviewer:** How should failures appear to users?

**Priya:** Not as a generic red banner that everyone learns to ignore. Users need to know which capability is affected, when it failed, what information may now be stale, and whether there is a fallback. At the same time, we cannot cover the map with technical errors during an emergency. The dispatcher and the engineer need different levels of detail from the same failure.

**Interviewer:** What security issues affect the design?

**Priya:** We have to assume that false observations and unauthorized commands are possible. A compromised civilian source should not be able to raise the regional threat level by itself. Dispatch and public-alert actions need strong authorization, but authentication cannot make the console unusable when people are wearing gloves, moving between stations, or working through an outage. We also need to limit access to sensitive infrastructure and responder-location data.

**Interviewer:** Operations wants changes quickly. How does that affect your team?

**Priya:** We cannot update every agency at once. New fields and message versions need to coexist with older integrations. A sensor provider might be offline during deployment and reconnect three days later with the previous format. We need gradual rollout, clear compatibility rules, and a way to test with realistic traffic before a change reaches an active center.

**Interviewer:** Who owns the meaning of fields such as threat level or available capacity?

**Priya:** That is often unclear. Engineering can implement a formula, but we should not invent operational policy. Does "available" mean physically present, staffed, fueled, reachable, and authorized? Different agencies answer differently. If the product team gives us a single number without defining it, the interface will create false confidence.

**Interviewer:** What would success look like from your perspective?

**Priya:** The system would degrade predictably, preserve an accurate record, and make data quality visible without paralyzing users. Teams could change one integration without surprising every response center. I would rather display an honest limitation than a beautiful map that quietly stopped receiving updates.

## Interview 4: Incident Commander

**Participant:** Colonel Elena Ruiz, incident commander for the Puget Sound Regional Response Center

**Context:** Elena is accountable for regional priorities during a kaiju event. She coordinates civilian authorities, military leadership, neighboring response centers, and public communication officials.

**Interviewer:** What information do you need when an incident begins?

**Elena:** I need to understand what is happening, what may happen next, and which decisions cannot wait. Where is the threat headed? How confident are we? Which populations and critical services are exposed? What response capacity do we have now, and what will we need if a second kaiju appears?

**Interviewer:** How much detail do you want on the main screen?

**Elena:** Less than the analysts want and more than a simple red, yellow, green indicator. I cannot read every sensor event. Give me the operational meaning and show me what changed since the last briefing. If confidence is low or sources disagree, that must be obvious. I also need to reach the supporting evidence when I challenge an assessment.

**Interviewer:** How do you prioritize response assets?

**Elena:** Protecting lives comes first, but that does not produce an automatic answer. Evacuating one sector can gridlock another. Committing every jet to Gorathos may leave nothing for a faster contact. Raising a barrier may protect downtown while redirecting the kaiju toward another community. I need to compare consequences, not merely see which target has the highest threat label.

**Interviewer:** Who should be able to issue commands?

**Elena:** Dispatchers need authority to keep operations moving within an approved plan. Strategic commitments, cross-border requests, citywide alerts, and actions with major civilian consequences require command authorization. If communications fail and someone uses emergency authority, I want them to act rather than wait, but the system must make that exception unmistakable afterward.

**Interviewer:** What concerns you about automated recommendations?

**Elena:** Recommendations can help us consider options we missed. They cannot hide value judgments. If the system recommends saving Seattle rather than Bellevue, I need to know what objective it optimized, what data it used, and what uncertainty it ignored. "The computer chose" is not an acceptable explanation to a mayor or a family.

**Interviewer:** What does the current coordination process miss?

**Elena:** Shared understanding. The analyst may update the projected landfall, but the evacuation lead is still working from the previous briefing. The dispatcher may know a unit is unavailable, while my status board still shows it in reserve. We spend too much time asking whether everyone is looking at the same version of the situation.

**Interviewer:** What should happen after the immediate crisis?

**Elena:** We review every significant decision. We need to reconstruct what information was available, what alternatives were considered, who authorized the action, and when the outcome became known. The record should include uncertainty and corrections. It must not imply that we knew at 09:10 what we only learned at 09:40.

**Interviewer:** How would you judge whether the production system is successful?

**Elena:** It should help the team make timely, coordinated, defensible decisions under pressure. A faster decision is not better if it is based on stale data. A complete picture is not useful if it arrives after landfall. The system succeeds when the right people understand the same situation well enough to act, while still recognizing what they do not know.

## Workshop Prompt

Working from the transcripts, decide what your team believes is most important to investigate or build first. Ground each claim in a specific statement from a stakeholder and separate what the transcript establishes from what your team is assuming.

As you work, consider:

* Who experiences each problem directly
* What outcome that person is trying to achieve
* What triggers the problem and what happens afterward
* Which constraints appear fixed and which might be negotiable
* Where stakeholders agree or conflict
* What evidence is missing

Do not attempt to solve every issue in one story. Choose a coherent slice that could produce useful learning during the workshop.

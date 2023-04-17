# Star Trek adventure

A choose your own adventure Star Trek game

- Pick a context to start with given 3 choices
- Follow story through, picking options
- How does it end?

## Coded LLM training

Proposed structure:

```txt
<start>
<choice1> You are the captain of the USS Enterprise. Your crew has ... </choice1>
<choice2> You are a vulcan on the USS Voyager ... </choice2>
<choice3> You are ... </choice3>
</start>

<scene>
<context> You are the captain of the USS Enterprise. Your crew has ... </context>
<desc> Your crew has just discovered a new planet, and you must decide whether to explore it or continue on your journey. </desc>
<optA> Explore the new planet. </optA>
<optB> Continue on your journey. </optB>
</scene>

<scene>
<context> You decide to explore the new planet. </context>
<desc> Upon landing, you encounter a friendly alien species who invite you to join them for a feast. </desc>
<optA> Accept the invitation. </optA>
<optB> Politely decline and return to the ship. </optB>
</scene>

<scene>
<context> You decide to continue on your journey. </context>
<desc> As you travel through space, you receive a distress signal from a nearby ship. </desc>
<optA> Investigate the distress signal. </optA>
<optB> Ignore the signal and keep moving. </optB>
</scene>
```

### A GPT-4 example

```txt
<start>
<choice1> You are the captain of the USS Enterprise. Your crew has just discovered a new planet. </choice1>
<choice2> You are a vulcan on the USS Voyager, seeking to establish a peaceful dialogue with a new alien race. </choice2>
<choice3> You are a Starfleet engineer on Deep Space Nine, tasked with repairing a mysterious alien artifact. </choice3>
</start>

<scene>
<context> You are a vulcan on the USS Voyager, seeking to establish a peaceful dialogue with a new alien race. </context>
<desc> The alien race, known as the Zentari, have agreed to meet with you, but you must decide which location would be most conducive to a successful dialogue. </desc>
<optA> Invite the Zentari to the USS Voyager. </optA>
<optB> Travel to the Zentari homeworld. </optB>
</scene>

<scene>
<context> You invite the Zentari to the USS Voyager. </context>
<desc> The Zentari delegation arrives, but they seem wary of your intentions. You must choose how to reassure them. </desc>
<optA> Perform a traditional Vulcan mind meld to show your sincerity. </optA>
<optB> Offer them a gift from Earth as a symbol of goodwill. </optB>
</scene>

<scene>
<context> You travel to the Zentari homeworld. </context>
<desc> Upon arrival, you are greeted by a large, armed Zentari escort. They insist on searching your shuttle before allowing you to proceed. </desc>
<optA> Allow the search to show your trustworthiness. </optA>
<optB> Refuse the search, as it goes against Starfleet protocol. </optB>
</scene>

<scene>
<context> You are a Starfleet engineer on Deep Space Nine, tasked with repairing a mysterious alien artifact. </context>
<desc> As you begin to work on the artifact, it emits a strange energy pulse. You must decide whether to continue repairs or consult with your superiors. </desc>
<optA> Continue repairing the artifact. </optA>
<optB> Consult with your superiors before proceeding. </optB>
</scene>

<scene>
<context> You continue repairing the artifact. </context>
<desc> The artifact suddenly activates, transporting you to an unknown location. You must find a way to return to Deep Space Nine. </desc>
<optA> Try to reverse-engineer the artifact's transport mechanism. </optA>
<optB> Attempt to communicate with the inhabitants of this new location for help. </optB>
</scene>

<scene>
<context> You consult with your superiors before proceeding. </context>
<desc> Your superiors recommend studying the artifact's energy signature before continuing repairs. </desc>
<optA> Follow their advice and study the energy signature. </optA>
<optB> Ignore their advice and continue repairs. </optB>
</scene>
```

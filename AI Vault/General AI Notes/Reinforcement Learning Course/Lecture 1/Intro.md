
An AI agent exists in an environment and it is trained through getting rewards.
There are sub-networks in RL:
**Policy Network:** Selects the next action
**Value Network:** Assesses the success of that action

The interaction with an environment has 3 phases: *<span style="color:rgb(0, 112, 192)">state</span>, <span style="color:rgb(255, 0, 0)">action</span>,* and *<span style="color:rgb(0, 176, 80)">reward</span>*. A complete cycle of these is called an *<span style="color:rgb(255, 192, 0)">episode</span>*. The final state of the environment is called the *<span style="color:rgb(0, 112, 192)">terminal state</span>*.

We can represent an episode in a single tuple:
$$ (s, a, r, s')$$
Note that we also include $s'$ here, which is the next <span style="color:rgb(0, 112, 192)">state</span>. This is like blockchain, where there is a link to the next state or "block in the chain".
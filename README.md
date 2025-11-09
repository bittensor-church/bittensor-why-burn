# Intro about the nature of staking in bittensor

Before we get tot he rules of burning, we have to get a common understanding on couple of things to explain who and why is causing the burn. This document is a (biased) perspective formulated by a subset of the Bittensor community, created to enhance the understanding of why the things are the way they are... But as you will soon learn, nobody can reliably predict what the decentralized hivemind of Bittensor holders is going to do! Here's how it works:

Tao and alpha holders delegate their stake to validators, giving them the ability to:
1. Validate and thus incur dividend rewards ("APY") for the holders
2. Be a tie breaker on the scheduled coldkey swap conflicts (it's a recovery procedure that can be used when a subnet owner or a validator gets hacked)
3. Run the validator code provided by the subnet owner, keep it up to date, provide it the necessary hardware... or not!
   1. Weight copiers don't run the code provided by the owner and there is not much we can do about it. They typically don't run any validation code provided by the owner and are purely interested in short-term gains. If every validator would become a weight copier, bittensor would collapse and die. Fortunately quite a few holders care enough about the ecosystem to not support them and nowadays the weight copiers are a marginalized minority and no longer a threat to the future of the ecosystem (because in 2024/2025 Opentensor Foundation and Church of Rao worked for about 1.5 years to change Bittensor so that the APY of weight copiers is below APY of the honest validators)
   2. The validator may decide whether it is in the interest of the holders to run the code provided by the subnet owner, or not. If, for example, the subnet owner is doing everything in their power to extract as much value from the bittensor ecosystem as possible while not providing any inteligence, they might choose to run the burn code (which basically turns the subnet off), preserving the value of TAO and protecting it from erosion from the exploitative behavior.
   3. The chain makes it so that the validators only have as much decision power as the stakers delegate to them.


Unlike in some other crypto ecosystems, in Bittensor the act of delegating the stake has major consequences both to the financial success of the staker:
1. If they delegate to a validator that performs poorly, their APY will be lower than it could be)
2. If they chose to stake into alphas, they can be affected by slippage, fees, alpha price depreciation... or alpha price appreciation. There have been instances of a staker having a 4000% return on investment in a couple of days (around sn14 release) and there were numerous instances of fraud and rugs.

Stakers in the bittensor ecosystem are _active_ participants. The success of their TAO investments DOES NOT depend solely on efforts of others - the decisions of when, where and to whom to stake have massive impact on performance of their portfolio (similar to active investment of USD in the stock market).


# Rules

You can click any of the `>` buttons below to see a more detailed explanation to find out why the given rule is here.

<details>
  <summary>
    1. Self-mining your subnet is prohibited unless your hotkeys are pinned to the subnet channel and you are keeping things fair.
  </summary>
  There have been numerous instances of subnet owners constructing the subnet in such a way that they incur all the rewards from it and it was not accepted by the Bittensor community. Those subnets were deregistered rapidly in pre-dtao times.
</details>

<details>
  <summary>
2. Centralized miner whitelists and blacklists are prohibited. Restricting mining by coldkey, axon IP, or IP range is prohibited.
  </summary>
A snippet from a discord conversation about this subject:
> Kat: I think some subnets are doing this because individuals are exploiting the subnet by deploying their exploit across large numbers of neurons.  Now, I would agree with you if you said, "okay, but they should fix their subnet mechanism instead of banning IPs" and I agree, because whack-a-mole is a losing proposition and wastes time.  But I also know that coding is not easy for everyone, and both finding and fixing the exploit can also be a process of finding something that works while not introducing another exploit.  Is there a balance to be found here, such as "this should be a limited tool, used to buy you time to fix the problem, and not a matter of routine application in lieu of fixing the problem"?
> Rhef: No, because when (not if) a subnet owner discriminates a miner for using multiple uids based on something that the miner can easily obfuscate, the miner will obfuscate it. Coldkeys are free, I have a script somewhere which produces 10 million coldkeys per hour per core. Axon IPs cost $5/month. Miners will defeat these measures in less than a day, but it won't be without cost.
> 
> If the miners obfuscate their coldkeys and IPs, we will lose transparency. From this moment onward in this subnet it will seem at a first glance that we have >240 unique miners, but that won't really be true, we'll only have a handful. Sooner or later someone will run a basic investigation using a block explorer only to find that all of those miner coldkeys actually send everything they earn to 2 or 3 wallets, and they'll tweet about it.
> 
> From the perspective of Bittensor ecosystem as a whole, that one day when miners adjust their operation to use multiple coldkeys and hotkeys is NOT worth all the twitter drama that will follow the investigations, therefore the subnet owners shouldn't selfishly employ measures which are trivial to defeat and harmful to transparency.
> Kat: I'm sure there are several owners doing this, and should know why it's a shortcut that's going to turn into a longcut, and why there are better ways to handle it.
> Rhef: I didn't say there is a better way to handle it. Nevertheless blocking by IP and coldkey is just harmful. You can blind yourself and say "I don't see any problems", but others will still see it and you will get caught. Don't do it.
</details>
<details>
  <summary>
3. Custodial burn wallets are prohibited.
  </summary>
  These can be commandeered illegally by the subnet owner or hacked. There are viable alternatives to this solution which are trustless and decentralized (Treasury contract, multi-sign wallets)
</details>
<details>
  <summary>
4. Using centralized solutions whenever the protocol supports a decentralized equivalent is frowned upon.
  </summary>
  This usually creates a single point of failure or an opportunity for the subnet owner to cheat. It is not really about the subnet owner cheating or not - the community can believe that they are honest, but they can be hacked or compromised. They can have the malicious employee, and there will always be a doubt on whether the subnet does what it is supposed to. 
</details>
<details>
  <summary>
5. Subnet code must be open-source, unless a prior exception has been granted by the burn police (typically for an anti-fraud module).
  </summary>
  TODO
</details>
<details>
  <summary>
6. Incentivizing miners to hold alpha with emissions is strictly prohibited.
  </summary>
  TODO
</details>
<details>
  <summary>
7. Any form of Ponzi or pyramid schemes are strictly prohibited.
  </summary>
  TODO
</details>
<details>
  <summary>
8. Obstructing TAO or alpha holders from validating — whether through hyperparameter manipulation or any other tactic, is strictly prohibited.
  </summary>
  TODO
</details>
<details>
  <summary>
9. Enabling or tolerating harmful or criminal services, including malware, CSAM, botnets and mixers, is absolutely prohibited.
  </summary>
  TODO
</details>
<details>
  <summary>
10. Validator code must actually work.
  </summary>
  One of the things that unfortunately happens from time to time is an unstable validator code owner says every piece of stake should be delegated to them because it's easier for them to manage the infrastructure and whatnot. But then they couldn't control over the entire subnet, and we have to trust that they run the code that is in the repository and not something else. This is not the way.
</details>
<details>
  <summary>
11. New miners must be able to join the subnet and survive the immunity process.
  </summary>
  TODO
</details>

# Consequences

1. Termination - If something is absolutely prohibited, then there's a great chance that the subnet is going to be administratively dissolved.
1. Punishment - If something is strictly prohibited, then an offending subnet is most likely going to find itself running skink code (1). If the slot is not sold quickly, it'll dereg soon.
1. Suspension - If something is prohibited, then an offending subnet is most likely going to find itself running burn code (2).
1. Other - If other offenses are found, the process of figuring out the reaction of the community to the given offense is more nuanced, but a rule of a thumb is "run burn code if there is doubt"

(1) sink code unstakes and all burns all incentive
(2) burn code burns all incentive

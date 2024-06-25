# Niche construction

The agent's world starts with a food patch (green) and multiple fertile areas (brown), including one in which a food patch sits.

Non-fertile areas are gray.

A food patch is surrounded by a light gradient the agent can learn to follow to find food.

When the agent spends time on a food patch, it absords food which replenishes its energy proportional to time spent metaphorically eating. If the agent's energy goes to zero, it dies.

Enough time spent on a food patch depletes the food which eventually reverts to merely fertile.

If the agent spends enough time over a fertile area some time after eating, a food patch later grows, centered on where the agent has spent most time. (The agent is metaphorically pooping fertilizer and seeds). The more time spent, up to the amount of time last spent eating, the larger the food patch will be.

If a food patch is not depleted (paler green), it eventually grows back to its prior state, whether or not the agent spends time (pooping) on it afterwards.

Hopefully, the agent would discover it can modify its world into a better food source by absorbing food without depleting it and then spending enough time on all fertile areas so as to turn them into food patches.

## Option: With poison food patches

A poison patch (red) can also grow in fertile areas. Eating poison decreases the agent's integrity without increasing its energy.

Similarly to food, a poison patch can be depleted and it can be replicated in another fertile area by the robot spending time on it after eating poison.

If food seeds are pooped on a poison patch, food eventually takes over the poison.

It is possible for a patch to contain, for a while, both food and poison (a mix of red and green tiles), and for the robot to eat of both.

Thanks to @eah13 for the idea!

## Option: With stygmergy

The agent deposits poop some time after eating and for a while proportional to the amount eaten.

If the agent spends a enough time eating, it will starting depositing on the patch it is on.

The robot can sense its own deposits (poop) and distinguish between the remains of poison (yellow) vs food (brown).

Deposits disappear on their on after some time.

Thanks to @eah13 for the idea!

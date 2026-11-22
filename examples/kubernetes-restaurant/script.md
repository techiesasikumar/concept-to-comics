# Example: Kubernetes

**Setup:** College students · Tamil Nadu · Tanglish

## Core truths
- **WHAT:** Kubernetes runs and looks after many app containers across many machines.
- **WHY:** You write the desired state ("always run 3 copies"). Kubernetes keeps comparing what you *want* with what you *have*, and fixes the gap: it replaces crashed copies and places new ones on machines with free space.
- **SO WHAT:** Apps keep running even when parts crash, without someone fixing things by hand at 2 am.

## Raw AI answer (viewer test case)

This is a full AI answer, pasted as-is, the way many people will paste it. It is kept on purpose as a test for the Comic Viewer, because it has things the viewer must **ignore**:
- text outside the comic (an intro line, and the "See it drawn for free" instruction with a URL),
- section headings like `Mapping table:` and `Next comics:`,
- an empty speech line (`Kumar: ""`).

Paste the whole block below into the [Comic Viewer](https://techiesasikumar.github.io/concept-to-comics/viewer/): you should get a clean comic with no empty bubbles and no instruction text in any bubble.

```text
Here's your comic! 👇

COMIC: Kubernetes
Subtitle: The manager who never sleeps
For: College students · Tamil Nadu · Tanglish
Characters: Arjun = boy, red shirt, medium skin | Kumar = man, white shirt, moustache, brown skin

PANEL 1 - Lunch rush
Scene: Busy mess kitchen. The board says "Always 3 dosa stations". Three cooks are working. Kumar the manager watches; Arjun, a part-time helper, is amazed.
Place: kitchen
Show: Arjun shocked, Kumar proud
Things: 🍳 x3, sign "Rule: always 3 dosa stations"
Kumar: "Rule simple: eppovume 3 dosa stations open!"

PANEL 2 - Oru cook absent
Scene: One cook goes home with fever. Only 2 stations are working.
Place: kitchen
Show: Arjun worried, Kumar thinking
Things: 🍳 x2, crossed 🍳
Arjun: "Aiyo! Oru cook fever-la veetukku poyittaar!"

PANEL 3 - Manager fixes it
Scene: Kumar compares the board with the kitchen, and calls a new cook to the kitchen that has a free stove.
Place: kitchen
Show: Kumar pointing, Arjun shocked
Things: sign "Want 3 · Have 2 → add 1 new cook", 🍳 x3
Caption: Kumar checks all day: what we WANT vs what we HAVE. Gap irundha, udane fix.

PANEL 4 - Idhu dhaan Kubernetes!
Scene: Arjun explains on a chalkboard.
Place: classroom
Show: Arjun proud pointing
Board: 🍳 Cook station = Pod (runs a container) | 🏠 Kitchen = Node (a machine) | 📋 "Always 3" = Desired state | 🧑‍💼 Manager = Kubernetes
Arjun: "So oru container crash aanaalum, Kubernetes pudhu copy start pannidum, users-ku theriyave theriyaadhu!"
Caption: You write what you want. Kubernetes keeps it true, 24x7.

PANEL 5 - Takeaway
Scene: The lunch rush is over and all 3 stations are running again.
Place: kitchen
Show: Arjun happy, Kumar happy
Things: 🍳 x3
Arjun: "Naama sollanum 'always 3'. Kubernetes adha 24x7 maintain pannum!"
Kumar: ""

Mapping table:
| In the comic | In real life |
|---|---|
| Cook station | Pod: runs your app's container |
| Kitchen | Node: one machine in the cluster |
| Board: "Always 3 dosa stations" | Desired state (e.g. replicas: 3 in a Deployment) |
| Manager comparing board vs kitchen | Kubernetes control plane, checking all the time |
| New cook in a kitchen with a free stove | A new Pod, placed on a node with free capacity |

Where this analogy breaks: Kubernetes never "repairs" the old cook; it starts a brand-new Pod. And it only opens extra stations in a rush if you set up autoscaling.

Next comics:
- What is a container (Docker)?
- What is a load balancer?

🎨 See it drawn for free: copy everything from COMIC to "Where it breaks" and paste it into https://techiesasikumar.github.io/concept-to-comics/viewer/
Want more? Reply draw (I draw a custom page, uses more of your chat limit) · prompts · or tell me what to change.
```

## Next comics
- What is a container (Docker)?
- What is a load balancer?

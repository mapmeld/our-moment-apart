# Cloud Atlas Bug

## The Starship

Mel woke up in the darkness. Instinctively he tried to move his arms and legs, but in the cramped space he could only stretch, which provided some comfort.

There was something that he had to remember here. Something something starship.

He heard the headset power off and on again with a metallic click. A few moments left for his own thoughts, his own reality, before dissolving back into VR-space.

## TapDanz Labs, Present Day

Phil opened the conference room door, nodded to the engineers who were poring over their MacBooks, and turned to see the source code projected onto the board.

“Do you have a marker? I was looking through the output-”

Several developers’ phones buzzed with another server-down notification.

“Stop scrolling. Can you jump to where that function is defined?”

“Which function?”

“This one that you’re calling here... right here.”

They followed a link to its place in the code, and from there into that function’s iterator. They puzzled over it a bit.

“Oh my god” muttered one of the interns. “It should be going up two at a time.”

“You’re comparing the first [x,y] pair, then instead of second [x,y] pair you’re looking at [y from first pair, x from second pair], and so on. Make sure the last iteration of the loop catches that, too, or we’ll be hanging forever for the callback.”

Half an hour later, the errant servers were back online.

Mallory tapped him on the shoulder. “That was cool how you could find a bug just like that.”

Phil shook his head. “There’s something else in there. You weren’t looking there before because that code shouldn’t be running at all, right? Not unless we’re being dumped there by another bug. That’s why we didn’t catch this bug during our review.”

“Well it didn’t make things worse, right?” She gestured to the break room and they sat in comfortable beanbag chairs. “Where are you seeing this bug living? Where do we find it.”

“It’s got to be something wrong on the client-side, in the headset. It might be running if the hardware failed to download initial point data, but any program should have all the data before it starts running.”

Mallory nodded. “It isn’t that big of a file.” She flicked through some new e-mails. “Time to call the hardware team, in Phoenix? I’ll email their team scheduler for an all-hands meeting.”

Phil shook his head, opened the email client on his laptop, and started typing.  “I just need one person.”

## University of Washington, 1979

Jane unspooled a stretch of masking tape and stuck one end on the study table. “One quarter inch off the end ought to do it.”

Her classmate deftly cut the end and placed it square over the two pencil-marked holes on his punchcard. “Will that do?”

“If you cover all of the other holes that we marked, sure. Don’t let it get too thick, or the reader won’t accept the tape anymore. And make sure to keep the cards in order in the carrier! And number them to be sure.”

The study room was buzzing with activity, people and coming and going even now, in the middle of the night. With the new mainframe in the lab, with FORTRAN 77 books appearing in the stacks, it was the best time ever to study electrical engineering.

As she got back to the dorms, there was one of the new Post-It notes pasted to her door: “Prof. Vaughn wants to speak to you at lab tomorrow morning.”

----

The professor was a caricature of a mad scientist - wild hair, giant glasses, and a not-quite-neat tie. Perhaps he aspired to the image. At the end of a long pronouncement to the other researchers at the table, he turned to Jane: “What’s your assessment?”

Jane had typed out several sheets of FORTRAN code. “When we fixed the first bug, the variable names, it doesn’t fix our overall problem. When you look at the loop, I think there’s an off-by-one error. I need to change both of them for this to work.”

The professor nodded, waited, and nodded again. Jane hid her exasperation.

“Jane, have you considered if it’s a problem with the compiler? If we received a bad compiler, I would like the university office to request a refund for our department.”

“No, not at all.” Jane was puzzled. “The real problem is that there are two different errors in the code which help hide each other, it just wasn’t apparent when we first looked.”

“Your code already has two errors?”

“Yes,” she admitted.

“Can you make a program which identifies problems like this, then? Errors which hide each other?”

“No, I mean… well, I don’t know for sure. But it would be quite valuable.”

The professor waved dismissively. “Fix the bug, rewrite the section, let me know what it looks like when it’s done.”

## Cambridge, UK, 1879

Charles Babbage was dead in the ground for years now, and neither the Difference Engine and Analytical Engine had been built. A professor at Cambridge had asked a young student, lost to history except for the name Thomas Falding, to help explain where the eccentric genius had failed in building the calculation machines.

Thomas had written in his first draft, “critical error - analytical thread returns to the wrong value storage column.”

“Thomas, we cannot simply say that it is the wrong value. Can you determine what the difference is, for an incorrect value? What is its distribution of errors?”

In a memo back to the professor, Thomas wrote, “It is off by one place, so in this case, we could call these mistakes off-by-one errors. Though if we are dealing with retrieving stored values, then the value recovered by an off-by-one error can be incorrect by a more significant number, and could answer the user with any number which the machine had previously stored. There is no distribution that can return from that kind of rror.”

Then a final note: “The main problem with the machine is an off-by-one error, except for a few times where I cannot trace where the logic has gone wrong at all.”

## National Science Foundation, 1980

Professor Vaughn took to the stage.

Jane hugged her friend Paula. “This is it!” They had worked for ages on posterboards explaining their code, which after a painful rewrite and deep dive into hex codes and overflows, was keeping accurate time with the National Atomic Clock.

“I would like to share some research going on in my lab,” the professor said, advancing the slide mechanism. “There was a team by two of our undergraduates, who created a timekeeping program.”

Their FORTRAN code flashed across the screen.

“Inadvertently, they discovered something quite interesting which I will discuss today - a potential for conspiring errors.”

The crowd laughed.

Jane’s face fell. Their one mistake, one year ago, was being highlighted over their successful project. The professor droned on about his code-checker, which sounded quite impressive to the audience, but Jane thought (it couldn’t be that simple could it?) that the code-checker script would only catch one kind of error.

“And we have the two student programmers whose mistake inspired us! Please stand!”

Paula and Jane looked at each other and stayed seated.

## Tapdanz Labs, Arizona branch, Present Day

“Professor?”

She smiled and stopped packing picture frames from the desk. “You can call me Jane by now.”

“I’ve been meaning to visit you. I heard that you are leaving the tech business.”

“Not just tech!  It’s time to retire. It’s been a long enough road for me.”

“Can I show you something from the Los Angeles office?”

“I suppose that’s the main reason you’re here.”

“Sure.” 

Phil found the right app on the tablet and opened up the blueprints. Jane removed her reading glasses from her coat pocket and started to flip through them. “Do you have crash logs?”

At Jane’s insistence, they printed the first one. She pointed at one burst of text. “Wow.”

“What about it?”

“I can’t explain it… but when I saw this bug I thought, there you are again! I have been chasing bugs like this my whole career.”

“What?”

She shrugged. “Look, a bug this deep in the hex code is bad news. It could even be a physical thing in one of the chips interacting with something in your software. I used to work on this type of stuff, and if I learned anything from that, it’s that you don’t want to go back there in the slog. And we don’t have to.”

“So what can we do?”

“I’m going to tell the incoming CTO to crush this bug by reflashing the chip in the headsets every 36 hours. If you’re in the middle of a game then, we can delay it and run for another eight before the device hits any serious bugs, in hour 44.”

“So they picked a new CTO?”

“I can pick my own replacement.” She handed him a crisp new business card. “Congratulations.”

## The Starship

Mel woke up in the darkness. Again he tried to move his arms and legs. This time there was something different… it felt like heat around his fingers and feet.

The VR headset did not re-engage.

It took an indeterminable time before he allowed himself to consider it: time to wake up. The door to his coffin-pod opened, and he staggered out, naked, into the cavernous hallway of the ship. Everyone around him was still numb and sleeping.

At the end of the hallway, he thought that he could see some other lights, but he didn’t dare venture far from the pod. It wasn’t allowed, he remembered. He turned back to his pod and saw a large piece of paper stuck to the neighboring door, a Post-It big enough to, yes, to uncomfortably wrap around his body, like a towel.

There was tiny writing printed along the edges, over and over again:
PROBLEM SHIP: CODE FIXER: MEL.

Damn them all to hell.

Wearing the post-it, Mel walked along the catwalk, holding the railing for support, and wondered if he could unfreeze another programmer to help him, or that would be NOT ALLOW HUMAN. Many things were NOT ALLOW HUMAN. The aliens and their ship knew a few phrases and used them repeatedly. They seemed to understand more advanced human speech... before the ship, his mother had whispered to him that they could read thoughts… but no one really knew where the disconnect was.

In an enormous neon atrium, the captain was in egg-pose. Perhaps the captain feared that Mel had a weapon, or maybe the ship was in more danger than he thought. A bright light appeared and almost blinded him. “What’s wrong?”

“CODE FIXER: MEL, ACCEPT.”

“I accept. That’s me.”

“NOT ALLOW HUMAN.”

“I don’t know the problem.”

A little red light appeared on his modesty Post-It. Begrudgingly, Mel took it off and stood naked.

“CODE FIXER: JEANINE, ACCEPT.”

In another corner of the atrium he could now see the woman, already holding a laptop and sitting on a stack of cardboard boxes. Unexpectedly, she laughed at the captain’s order.
“I accept my new friend Mel.”

“CODE ROOM”.

Jeanine stood and beckoned Mel to follow.

-----

In a smaller, human-sized room, Jeanine pointed out a large floor screen, which had several circular windows of scrolling code.

“Jeanine… can you follow this?”

“Yup, I’ve been looking at it for several days now. Captain agreed that I could wake you up.”

“Are we… are we doing the right thing, fixing this? I thought the plan-”

“I fucking remember the plan, okay?” Jeanine clenched her fists. “This isn’t from our people or whatever. It’s a bug in the hypersleep code, and if we have to wake everyone up, it would be bedlam, there wouldn’t be enough space or food or water. I thought about it a long time.”

“Maybe this is the plan? I know it isn’t ideal, but if we don’t make it to the destination, we don’t work for them, their little enterprise is over.”

“I’m not killing everyone on this ship!”

Mel looked away, not having seen a real, human, emotional reaction in years of VR-space. Had he forgotten how to argue? Did he want to save everyone? It seemed like a good idea to try and save everyone’s lives.

Jeanine opened the next window. “As best I understand it, their ships have been running for thousands of years without incident. Our human-coded program got put in about twelve years ago, so they have a pretty good case for it coming from us.”

“Twelve years?”

“Yes, first things first, we’re twelve light-years from Earth, so don’t talk to me about hitching a ride back or Captain America Starship coming to tow us home. Second thing, I need your opinion on this. This is why you’re awake. Accept?”

“Yes, accept, as long as they reboot the alien computer every thousand years or so, downloaded their Windows XP service packs, it does seem like the human code would be the problem.”

She smirked. “So you can have a little fun with this assignment.”

-------
Time stretched as the two pored through lines of code. Fortunately the programmers who made the connection library between alien and human technologies had the best intentions and good code-commenting practices, so they were able to draw the structure out on Jeanine’s Post-It.

“Okay Mel, any theories?”

Mel had finally picked up the method behind the floor screen controls. He pulled up the VR headset header file. “Some people had a bug in their commercial headset and put in a reboot to get around it. We know that because in hypersleep we come out every 36 hours.”

“Good. And when did that code get written?”

“Many years before the alien visits. Yes, I get it. It wasn’t planned like this.”

“Thanks. Now how does a bug in a VR headset get propagated up into the main ship computer?”

“Do you know it, Jeanine? Because I didn’t get that far.”

“A lot of the code is about consistent timekeeping, and it’s tough when traveling at relativistic speeds.”

“I could see the VR headsets receiving a time from the ship computer, but why would the ship want the headset to tell the time back? We are all traveling together at about the same speed.”

“Well, that’s the part that I still don’t know.”

-------

They were sleeping in the room, back-to-back for warmth, when a siren sounded.

“CODE FIXER: JEANINE: EXPLAIN.”

“Oh God, they’re going to drop a nuke. Get in brace position up against the wall.”

Mel sat up and crawled over to a wall. “What?”

“The ship propels itself with nukes, it uses sort of a pusher shield to move it forward.”

“Are you serious? I don’t think that they did that before?”

“Because around Earth they used their little rocket motors. Big acceleration from the nukes. You’ve slept through the last hundred or so. Hold on!”

Mel expected a sound from the bomb, but instead the ship lurched forward and continued on.

------

Mel waved Jeanine over. “Look at the two headset clocks.”

They had disassembled the devices, a little anxious about where they had come from, until they supposed they were from their own pods. They had plugged the devices into the alien logger.

“After the jump, the ship computer asked both of these headsets what time it was,” Mel explained, “but we told our headsets not to send anything back, so all’s good.”

“Okay.”

“I’ve been keeping this one from rebooting. What’s interesting is that the headset clocks no longer match. By a huge amount.”

“What’s that about?”

“The ship is asking our devices to keep track of the local time, Earth-time specifically, independent of our relativistic speeds. All of that detail about our planet and solar system would be human-coded.” Mel pointed out the two devices. “Depending on whether you’re mid-reset or maybe not resetting at all, after the jump, there are errors. What do we do with errors?”

“We check the distribution of errors and see if they are predictable?”

“Well, this ship averages them. The bug could even be on their side… maybe they didn’t expect us to screw up so badly.”

Jeanine laughed and took the controls. She looked over the code for a long time. “So I mean, we can fix this, right?”

“We don’t know the real time anymore, though. We might not be twelve light-years from Earth.”

Jeanine paused. “The ship uses stars or pulsars to know its position, since those don’t change so much. You’re just right about the home-time.”

“How could you know that, though?”

“I have looked at this for a long time, okay?” Jeanine slipped to the floor and held her knees to her chest. “I started with displaying the code so we could see it and edit it. Then I was fixing location, since something made that wrong. I guess it was this Earth-time bug all along, all ten years I was working on this.”

“What?” Mel stepped back and hid his own nakedness. “So you are okay working with them?”

“No, I just… I don’t want everyone to die. I was thirteen and I was tired of the VR headset, so…”

“Ten years and you just asked for help now?”

“I didn’t want to wake up some older guy who was going to tell me what to do. They taught me their code, and I waited until I knew my stuff and you, well, until you weren’t so much older.”

“Five minutes. I need five minutes to process this and... puke or something.”

“Have you ever puked?” Jeanine brimmed with bizarre curiosity.

------

Mel stood before the massive transparent window, where the captain stared out into space. He was still in egg-pose.

“Ten years?” Mel shook his head and banged his fist on the window. It felt surprisingly soft and fabric-like.

“NOT ALLOW HUMAN”

Mel stepped back and shouted, “We fixed your bug! Jeanine will figure the rest out pretty soon, I think. You have the resources and the starship, and you still want us to come and do the dirty work. Don’t you have alien triple-A or an I.T. hotline or something?”

“NOT ALLOW CAPTAIN”

It was a new phrase. There was a being that could NOT ALLOW CAPTAIN?
“Would you like to explain that?”

“NOT EXPLAIN”

“I would just storm off, but if you’ve been sitting here for ten years, I suppose you would just keep waiting. You’re welcome.”

There was no answer from the giant egg.

--------

Jeanine was still flipping through holographic sheets of alien code, with a view which Mel supposed she had coded herself.

“How did your talk go with the captain?”

“He said that we did a really great job, and we are all going for ice cream later.”

“Is that right?” Jeanine smiled. “I remember what that means.”

“Don’t you wonder what will happen to us? You didn’t find a loophole this whole time?”

“Listen, I am working on it!”

“We just-”

“Trading routes. Interstellar trading routes and regulations, okay? Why don’t you read something? We can’t afford to be ignorant about the galaxy.”

------

“Let me show you something in the human-code,” Jeanine said.

They looked over a few files, and then she pulled up an environment variable file.

“They encrypt all of their variables in the code room console, so if the ship computer gets a virus, only an admin can physically access the keys.”

Mel nodded and shook with anticipation. They opened the document.

```
KEY=HELLO_MEL_THIS_IS_JEANINE_AND_THE_REST_IS_GIBBERISH_EQ491293...
```

“This makes sense, I will be able to decrypt things now.”

“There’s more.”

```
PLAN=Trade routes! It is ILLEGAL for CAPTAIN to be shipping us! They rescue us!
TIMEOUT=
```

“We set a timeout here,” she explained, “until the ship deccelerates and makes its final course correction into port. Can you tell me what the orbital program told you?”

Mel nodded. “Twenty-one years, and fifty-two days.”

Jeanine typed this value:

```
TIMEOUT=9.years + 24.days
```

“Will that convert to ship time units? It seems weird to use Earth units.”

“Yes, that should do.” Jeanine saved the file.

The alarm sounded. “SLEEP: MEL, ACCEPT. SLEEP: JEANINE, ACCEPT.”

“Good night. Well, see ya in twenty-one years.”

Again. “SLEEP: MEL, ACCEPT. SLEEP: JEANINE, ACCEPT.”

“Good night. Sleep well.”

They exited the room and went separate directions. The headset had been replaced in Mel’s pod. He stepped in, and as the doors closed, thought of the little electrical pulses unwittingly steering them to safety.


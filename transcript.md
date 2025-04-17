# Transcript

## Informal intro

Thank you Professor Kirby, and hello everyone. My name is Ben Allen, and the first thing I want you to know about me is "I used to have hair".

This is a graduation picture, and this is how my Mum likes to think I spent my days at St. Andrews. In formal dress, white tie & gown.

This is how I remember my time at St. Andrews. Collapsed on West Sands, with a bottle of Kronenbourg close to hand.

## Formal intro

I loved my time at St. Andrews, and following graduation I started the rollercoaster which is a career in software engineering and product development. My first job was with a digital agency called HeathWallce, and we specialised in usability and accessibility when absolutely no-one knew what those terms meant. We used to pitch for business in big conference rooms with the best & brightest digital minds and spend 30 minutes explaining that "perhaps you’d sell more if your product was easy to use". Mind blowing.

That experience within my first job ended up playing a huge role in my career.

## My experience in digital accessibility

You see, I’ve been working in the software industry for 21 years, 15 of those years working in the USA, and most of that time has been spent in the accessibility field. I was a software engineer for 3 years, building user interfaces that were extensively tested for accessibility. Later, I became a Program Manager responsible for implementing accessibility testing programs at large companies like PNC Bank, and GitHub. Today, I’m in Product Management. I work at Deque, and help build tools for product development teams who are trying to incorporate accessibility into their software products.

## Accessibility intro

Today I’ve come to talk to you about the subject of accessibility: what it is, why it’s important, why it’s hard, and how to do it. Like all topics in computer science, this is a vast subject. A lot of these ideas, for the sake of brevity, will be introduced and not explained completely. I’ve prepared a GitHub repo with links to lots of resources so you can do your own follow-up research, and I’ll be available for Q&A after this talk. The link to the repo will be provided at the end, and that will include a transcript of the words I’m speaking today.

## What is it?

So, what is digital accessibility?

- QUESTION: raise your hands or say "aye", who’s heard of accessibility?
- QUESTION: keep them raised or say "aye" again, who has built or tested a product for accessibility?
- QUESTION: keep them raised or say "aye" again, who really believes I had hair in my early 20s?

Digital accessibility is rooted in usability. It’s about making digital products easy to use. To expand on that, it's the process of understanding how people with disabilities engage with digital content and, given this understanding, making products easy to use.

### Disability

Let’s dig into this statement a little bit and think about the disability part first. There are all kinds of disabilities out there. We tend to focus on 4 broad categories: vision, audio, motor, and cognitive disability. Within each category there is a broad spectrum of disability. For example, short & long sightedness would be in the vision category along with "legally blind". They’re just 2 ends of a broad spectrum.

Let’s think about some more examples:

- First, visual ability - think about low vision, colour blindness, blindness
- Second, audio ability - think about hard of hearing and deaf
- Third, motor ability - think about the use of limbs. You may have lost a limb or you may have a tremor and you can't use a mouse.
- Finally, cognitive ability - think about reading ability, your ability to focus on a task, perhaps even your ability to handle flashing content.

A lot of times when we speak about disability, people assume we are only talking about life-long disabilities or something you’re born with. This also ends up being a spectrum. Sure, people have permanent disabilities, but disabilities can also be situational, or temporary.

If you’ve broken your arm, for most of us, that’s a temporary disability. If you’re preparing raw chicken in the kitchen, you might have dirty hands, that’s a situational disability. In all these cases, you will use technology differently to accommodate your current level of ability.

QUESTION: can you think of other examples of situational disabilities? How do you use technology differently?

DEMO: W3C video

### Assistive technology

This is a good time to start talking about how people with disabilities engage with digital content. In some cases, differences in interaction might be small. A person who is deaf will consume digital content just like someone with no disability except for when they engage with audio or video content. In that case a deaf person will need captions to figure out what’s going on. Of course, if they know sign language, they might prefer to have a signed version of the spoken word.

People with visual disabilities will use a range of different assistive technologies. People like me will use glasses when reading the web, or request that a presenter makes their text larger when giving a presentation over Zoom. If we keep going along the visual disability scale, you start to see bigger differences. People who are blind will use something called a screen reader. A screen reader takes content presented visually on the desktop and web and converts it into audio so a person who is blind can consume that audio content.

DEMO: screen reader

There is a long list of really interesting personas at the W3C, and these personas will introduce you to all sorts of assistive technology. The thing you should takeaway is that different people engage with the web in different ways and there are things we can do, as digital content creators, to make it easier for those people to consume and interact with that content.

## How do I do it?

At this point, you might be thinking this all sounds great but "how do I know what people with disabilities will find usable?". If I have my QA hat on for a second, a lot of QA involves a nice list of functional requirements which I can build test cases for, and then test against. It’s totally reasonable to ask: where’s my nice list?

In accessibility, our list of requirements comes from a standard called the Web Content Accessibility Guidelines or WCAG for short. The standard is created and maintained by the W3C, and we’re currently at version 2.2.

Version 1 of WCAG was published in 1999 so our measuring stick for accessibility has been around a long time and the guidelines change very slowly. It usually takes between 5 and 10 years for the standards to change.

DEMO: BRING UP WCAG AND SCROLL THROUGH IT.

WCAG is made up of 4 principles, usually called the POUR principles. That stands for perceivable, operable, understandable, and robust. WCAG has 13 guidelines, and each guideline has testable success criteria. Each success criteria has 1 of 3 levels: A, AA, and AAA.

The levels are cumulative too. To get level A conformance you need to meet all level A success criteria, to get level AA you need to meet all level A and AA success criteria. Finally, to get AAA conformance you need to meet all success criteria.

Companies pick a standard and a level, and test against those success criteria. Most big companies these days will pick WCAG 2.2 level AA. Their QA teams will test against all relevant success criteria marked as level A and AA. If the digital interface under test passes those criteria then they are considered compliant with the standard at that level.

DEMO: seeing the levels in the guidelines, filtering the guidelines.

But wait, there is more! We don’t just get a list, we get a guide on how to test each thing in the list. Different companies have different testing methodologies but one of the most popular is called “Trusted Tester” from the US Department of Homeland Security.

## Why is it hard?

Awesome, now I have my list! I can test all the things. This is going to be easy, right?

Let’s take a quick survey of the top 1 million websites and test against a small sample of the WCAG success criteria and learn some stuff. Surely, everyone nailed this. After all, they have a nice list! The WebAIM million is exactly that. 

DEMO: pull up the WebAIM million.

- Question: who has heard of The WebAIM million?
- Question: what do you think the average number of errors per site was? Raise your hands or say “aye” if you think they found 10 errors or more on average?
- Question: keep your hands raised or say “aye” again, if you think they found 20 errors or more per page? 30/40/50/100?

The correct answer is 51 errors per page; and just to remind everyone, they were testing about a quarter of the success criteria within WCAG. What the heck is going on?

There are many reasons why making content accessible is hard. I’ll start with 2:

- The skills gap
- The empathy gap

The skills gap is really clear. Accessibility is rarely taught at university level computer science, or coding bootcamps. In my experience, the vast majority of product managers, designers, developers, content writers, and QA don’t know anything about accessibility, or simply have a beginner level of knowledge.

The empathy gap might be more important. Empathy is the “ability to understand and share the feelings of another”, and in my experience, it’s hard for product development teams to put themselves in the shoes of people with disabilities. Ability is such a broad spectrum. How can people start to appreciate all the different ways in which people with disabilities interact with the digital world? It’s harder still when you’re in your early twenties, and perhaps at the peak of our physical ability.

In some ways it’s a vicious cycle. If digital accessibility is bad, we’re making it harder for people with disabilities to get great jobs, and to become colleagues and team mates. If we’re not working or going to school with people with disabilities, we have limited opportunities to empathise. If we can’t empathise, perhaps we lack motivation to learn, and digital accessibility keeps getting worse.

A third reason why accessibility is hard is automation or the lack thereof. Today, you can’t automate your way out of an accessibility problem. It’s just not possible, yet. The best tools out there can test between 20-30% of WCAG. Of course, there is more than 1 way to count coverage. Instead of counting success criteria, you can count all of the issues you found during testing and work out how many of those issues could have been caught by automated tools. If you have a big sample of tests, you get a better read on the true value of automation. Deque has a huge sample of test data and they suggest that coverage can be counted by “issue frequency”, and that number is around 50% for purely automated tools, and ~80% with semi-automated tools. In other words, automation that needs a little help from a human.

A fourth reason why accessibility is hard comes down to basic economics: incentives. The incentives surrounding accessibility are not strong enough. Put simply, the lack of accessibility will not put you out of business. Let’s compare that with other non-functional requirements like security or privacy. If you’re a big bank and you get hacked, that will impact your stock price. Banks invest in security not because they think it’s morally or ethically sound, they invest because they don’t want to lose in the stock market, and they don’t want to see bus loads of customers walk to the bank next door.

- Question: raise your hand if you’ve ever read or watched a news article discussing a security breach that impacted a company’s stock price?
- Question: keep your hand raised if you’ve ever read or watched a news article discussing accessibility non-compliance and how that impacted a company’s stock price?

## Why should you do it?

In the accessibility industry, we still spend a lot of time and energy convincing senior leadership of different companies that accessibility is worth doing. So, beyond good ethics, what are the reasons to do accessibility?

- It’s better for everyone, not just people with disabilities. A more accessible site is a more usable site for everyone. This sounds counter-intuitive but it’s true. Many accessibility features end up solving problems most people care about.
  - We all enjoy text with good colour contrast.
  - If you’re watching a video on YouTube, it’s easier to search for the thing you’re interested in by searching the transcript.
- Search Engine Optimisation (SEO) - one of the first accessibility training sessions I went to described it this way “the biggest user of the Internet is deaf and blind. It’s called the googlebot.” Accessibility is great for SEO.
- More revenue by increasing your addressable market - people with disabilities have money too!
  - The World Bank estimates that there are at least one billion people – 15% of the world’s population – have a recognised disability
  - Those 1 billion people have a spending power of more than $6 trillion. They have power to impact your revenue and they are willing to use it.
- A larger talent pool. There are so many smart, creative, determined people with disabilities ready to work for the right employer.
  - I used to work for a CEO at a big bank who believed that the company “was at war on talent”, and he strongly believed in the potential for people with disabilities to be a differentiator.
- More diverse teams. There is research that suggests that more diverse teams are higher achieving.

### The Law

Finally, we have to talk about the law. When markets fail, and when bad outcomes become normal, the law can help correct behaviours by realigning incentives. This is a really big deal for accessibility. America has the American’s with Disabilities Act, or ADA for short. Europe has the European Accessibility Act, or EAA for short. These laws make it a requirement for companies to provide accessible content. It turns out that companies and government institutions don’t like getting sued. So many companies out there will fund large accessibility programs to avoid the risk of litigation, the costs and the brand harm that comes with it.

Moving past the academic, I want to share a personal story when things clicked for me. I was running digital accessibility at a big bank. Each year the bank ran a big internal accessibility conference. It covered digital accessibility, cash point accessibility, the accessibility of the many buildings and branches we owned. It was really cool.

By this point, I had been doing accessibility for over 5 years and I was super confident. I knew all the theory surrounding digital accessibility, my team were growing, and my team were having an impact.  I felt like a big deal at this conference and I volunteered to host an innovation workshop. It would contain about 12 people. I spent weeks researching different workshop techniques. I bought a copy of Thinker Toys and I drinking chapters. I had all these sessions planned for getting the creative juices flowing, and all I needed was a box full of markers and different coloured sticky notes.

The day before the workshop I felt super confident until someone asked me: did you prepare for the people with disabilities in your group? Folks, I went pale. I felt sick. You see my expertise is in digital accessibility. The digital world, not the physical one. BUT, oh my goodness, I should have known better. With less than 24 hours to go, I was pretty sure my career was over. I’d be found out. I’d be a fraud. Luckily, I was meeting a colleague for dinner that night, and she was gracious enough to share her wealth of experience in working with people with disabilities in the physical world. I felt calm and prepared again.

The next day, I ran my innovation exercises. I split the group into 2 so we could bounce ideas between teams. As luck would have it, 1 team had a bunch of "fully able", legal and compliance types. Very smart lawyers and people like that. The other group had people who were blind and people who were hard of hearing. After a day in that workshop the group with disabilities outperformed the group of lawyers. They came up with better ideas and drove better discussion. It was then that I understood the value of empowerment. I finally got it.

If you can empower people with disabilities by giving them equal access to information and tools, they will deliver. They will contribute to our businesses, our communities, our culture. They will have the means to lead more independent lives.

## Thanks and goodbye

I hope this has given you a good introduction into digital accessibility, and I really hope you explore the subject more and empower others to build accessible content. In addition to accessibility, I wanted to speak a little bit about how QA has evolved in my career.

Do you have any questions?

Thank you so much for having me.

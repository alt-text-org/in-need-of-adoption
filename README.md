I am dying, and have accessibility projects that need leadership if anyone is able
===

I have made a number of prototypes of unique accessibility projects over time, which I will not be able to work on or manage in any way in the time I have left. I have a large brain tumor which severely impairs my focus, memory, and executive function. I'll list projects here, with links that are relevant. If you have questions please reach out via email or make an issue here.

About me: I tripped into accessibility work specifically around alt text on social media, specifically Twitter, building a bot (AltTxtReminder) for quick, polite, private messages when folks forgot alt text on images. Its success was a called out reason for Twitter shifting effort to building that functionality into the platform, it has since been permanently banned. I also made another bot (AltTextUtil) to be a swiss army knife, primarily used for OCR, it would now cost $5000/month to run. During that time I was on a small board of external developers maintained by Twitter to advise on API changes, and did my best to be an advocate. I’ve built two teams trying to implement http://alt-text.org, a library searchable by image for human-written alt text for frequently used images such as memes, with a focus on providing an API so screenreaders could easily use it. At a later point I found I tried during all that time to network, but I am Autistic and had a large tumor I didn’t know about, impairing my abilities. I am now struggling to do any work requiring focus without hyperfocus, and I don’t get to choose what gets that, so my communications will be impaired, and multiple pings may be necessary. I have hyperfocus for a draft right now, so this is a draft.

Contact
===

I can best be reached here or via email at hannah@alt-text.org

Projects
===

Alt-Text.org
---

I try to provide tools to make doing the right thing easier. The http://alt-text.org project is on pause for its MVP https://my.alt-text.org, a site designed for writing alt text for images, with a private and computer-local library. The grander scheme is a site and API for lookups in a library of alt text by image, for usage by Visually Impaired folks for un-described images, and those describing images on social media to either start from a prior description or use it, where the latter would often have described it less usefully if at all. I believe this is useful for images such as memes, which frequently spread or are re-used with little manipulation
I built a working prototype website and API, now down, and exposed them via a Twitter bot as well as allowing folks to sign up such that anything they posted would have its alt text added. It faces legal issues around copyright and moderation issues, among others. Everything is a prototype, and I was very much learning as I was going with JavaScript and frontend dev.

I was the engineering lead on the team that maintained the busiest APIs in the company, with 5 billion active users and 200k requests/s. I built the backend on cloud services, and I built it to scale and for cost to scale with usage. I believe folks may be able to convince GCP to provide discounts.
The private library MVP is offered through a site with the aim of being used in an iframe or browser extension or app. I was partway through writing a prototype when I ran out of hyperfocus and dropped the project. https://my.alt-text.org is the site, and https://github.com/alt-text-org/my.alt-text.org the code. A future stage could build the API and offer to import peoples private libraries or search the public from the site. The current implementation misses a feature I realized later: users should have private as well as public libraries, and import/publish from private.

Prototype JS API repo: https://github.com/alt-text-org/js-api.alt-text.org

NodeJS was used for the backend prototype as I could only find the chosen fuzzy image matching algorithm in JS. The implementation was incredibly slow, and while I improved it 3x with some code changes, it's still slower than the ideal. I have since implemented that algorithm from scratch in Rust, and while JS took seconds, Rust takes tens of milliseconds. The project is available via Cargo, and needs a maintainer, ideally soon as a bug has been found. The code is available here: https://github.com/alt-text-org/image-match-rs

Site repo: it is not accessible: https://github.com/alt-text-org/www.alt-text.org


Non-Linear OCR
---

I explored using Google’s advanced OCR API to extract text from images where text is grouped rather than linear, such as text tables or comics into HTML tables for navigability by screen reader. There’s a rough draft of it available for use at https://2d-ocr.glitch.me or its code is at https://github.com/alt-text-org/2d-ocr

A similar usage could be specifically targeting extracting text from dialogue in comics usable both via screen reader and by folks writing alt text to allow more attention to the visual elements.


Mozilla Developer Network HTML/CSS Accessibility Documentation
---

I discovered by accident that the MDN web developer documentation was inconsistent with its accessibility sections. Specifically I found that the datalist HTML element, which I was considering for a project, had docs that moved accessibility concerns to the bottom of the page below sections unlikely to be examined. I was considering it for a project around accessibility, and only found by accident the docs saying that browser magnification ignored sub-elements, rendering any usage of datalist inaccessible.

In starting the conversation with the MDN maintainers and examining the broader list of accessibility sections in various element docs I found inconsistent location and formatting, and on some examination have proposed a plan for improving things that's been met with unanimous approval by the developers, though they have not prioritized it. This project has the potential to improve the accessibility of large chunks of the internet and to spur similar documentation improvement elsewhere.

Discussion: https://github.com/orgs/mdn/discussions/430

The datalist docs have improved, but not to the hoped for or planned level: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist#accessibility_concerns


Discussion, with plan: https://github.com/orgs/mdn/discussions/430

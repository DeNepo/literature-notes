# Analyzing Fine-Grained Material Usage Behavior, Koutcheme et al, 2021

2 pages

available at: https://cssplice.github.io/SIGCSE21/proc/SPLICE2021_SIGCSE_paper_4.pdf

[the paper](the-paper.pdf)

In contrast to previous research, using IDEs themselves to gather log data on student activity, this study looks at logs from online textbooks (and web-based materials in general).

Most interesting part is the actual log data, comprised of
- User Id
- timestamp
- event type
- first visible element
- last visible element
- top Y coordinate
- page URL

Presumably, this involved students who had opted in to data collection, since they were only collecting data in one class, though what if we wanted a general method to push data like this to a central system. The biggest issue would probably obtaining consent, and how to phrase it, since most people are now familiar with the GDPR-cookie consent popup (at least in the EU), but would we have an additional popup or just assume the consent for cookies equals consent for this other type of data collection? In theory, as long as there is no personally identifiable information, then we wouldn't be beholden to GDPR compliance requirements, but it's unclear what data we would be interested in, so making that determination is a bit difficult.

The original javascript component used involves jquery, though if we used something like open telemetry (https://opentelemetry.io/docs/instrumentation/js/getting-started/browser/), that might be a bit more robust. It would also allow for a uniform format of data pushed somewhere.

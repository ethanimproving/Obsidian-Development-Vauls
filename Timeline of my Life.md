---
dg-publish: true
---


# Personal

`Alt + Scroll` to zoom.

```timeline-vis
tags=personal
startDate=2016,10
endDate=2019,5
minDate=1990
maxDate=2030
```

View YouTube History in the [Google Activity page](https://myactivity.google.com/product/youtube?hl=en).

# Crushes

```timeline-vis
tags=crush
startDate=2002
endDate=2020,10,10
minDate=1996
maxDate=2030
```

The `vis-timeline` library in node.js has a Timeline object that takes a list of DataSet objects. My dataset is as the following:

```
{
	id: items.length + 1,
	content: event.title ?? '',
	title: noteCard.outerHTML,
	start: start,
	className: event.class ?? '',
	type: event.type,
	end: end ?? null
}
```
The Timeline looks like this:

```ts
export class Timeline {
  constructor(
    container: HTMLElement,
    items: DataItemCollectionType,
    groups: DataGroupCollectionType,
    options?: TimelineOptions
  );

  constructor(
    container: HTMLElement,
    items: DataItemCollectionType,
    options?: TimelineOptions
  );
```

I'm sure you can find it online if you search. Each dataset creates a `vis-item` HTML object. Is there a way for me to wrap that HTML object in an a tag with an HREF? It's complicated because it's the `vis-timeline` that's rendering the HTML, which I am not very farmilear with. Can you help me?



Currently I have a `block.ts` file that is being used by an Obsidian Plugin to create events in a timeline.  Each event is rendered as the following HTML:

```html
<div class="vis-item vis-range pink vis-readonly" style="transform: translateX(56.04px); width: 148.632px; top: 237px;">
    <div class="vis-item-overflow">
        <div class="vis-item-content" style="transform: translateX(0px);">
            <div>Crush on Savannah Calvert<div class="timeline-card pink">
                    <article>
                        <h3><a class="internal-link" href="/Timelines/Crush on Savannah Calvert.md">Crush on Savannah
                                Calvert</a></h3>
                    </article>
                    <p></p>
                </div>
            </div>
        </div>
    </div>
    <div class="vis-item-visible-frame"></div>
</div>
```

If I provide the `block.ts` file to you, can you modify it so that it moves the vis-item *inside* the internal-link? Such as:

```html
<a class="internal-link" href="/Timelines/Crush on Savannah Calvert.md">
    <div class="vis-item vis-range pink vis-readonly"
        style="transform: translateX(56.04px); width: 148.632px; top: 237px;">
        <div class="vis-item-overflow">
            <div class="vis-item-content" style="transform: translateX(0px);">
                <div>Crush on Savannah Calvert<div class="timeline-card pink">
                        <article>
                            <h3></h3>
                        </article>
                        <p></p>
                    </div>
                </div>
            </div>
        </div>
        <div class="vis-item-visible-frame"></div>
    </div>
</a>
```

It is using the `vis-timeline` library. Don't create any code until you've seen the file I want you to modify. Do you understand?

# Salvation

```timeline-vis
tags=salvation
startDate=2015,11
endDate=2016,10
minDate=1996
maxDate=2030
```

# Plans

```timeline-vis
tags=plans
startDate=2019
endDate=2021,10
minDate=1996
maxDate=2030
```

```dataview
table start-date as Start_Date, end-date as End_Date
from "Goals/Timelines"
sort Start_Date desc
```

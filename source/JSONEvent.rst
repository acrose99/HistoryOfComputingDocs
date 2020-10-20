The JSON Structure for Events
===============================
We dynamically render each event through a locally stored JSON file called events.json.

It is unordered for the sake of convenience for George/Dennis/history people.

**However, George and Dennis will need to follow this format**

The JSON code
--------------
    .. code-block:: javascript

      {
        "id": 3,
        "Type": "OldComputer",
        "Title": "Hewlett Packard introduces the HP-35",
        "Body": "The Macintosh 128K, originally released as the Apple Macintosh, is the original Apple Macintosh personal computer.\n\nIts beige case consisted of a 9 in (23 cm) CRT monitor and came with a keyboard and mouse. A handle built into the top of the case made it easier for the computer to be lifted and carried.\n\n It had an initial selling price of $2,495 (equivalent to $6,140 in 2019).\n  \nThe Macintosh was introduced by the now-famous $370,000 (equivalent to $910,541 in 2019) television commercial directed by Ridley Scott, ‘1984’, that aired on CBS during the third quarter of Super Bowl XVIII on January 22, 1984.\n\nSales of the Macintosh were strong from its initial release on January 24, 1984, and reached 70,000 units on May 3, 1984. Upon the release of its successor, the Macintosh 512K, it was rebranded as the Macintosh 128K. The computer is Model M0001.",
        "Date": 1972,
        "Location": "Palo, Alto, US",
        "Citations": [
          "Tim Apple",
          "Michael Fassbender"
        ],
        "TimelineImage": "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.a_cRAdX47acRF2DXVwcF6AHaHb%26pid%3DApi&f=1",
        "EventFocusImages": [
          "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fmacgateway.com%2Fwp-content%2Fuploads%2F2011%2F02%2FOriginal-1984-Apple-Macintosh.jpg&f=1&nofb=1",
          "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcompidiaries.files.wordpress.com%2F2014%2F01%2Fmac1984.jpg&f=1&nofb=1"
        ]
      }

Fields
----------
* ID: This currently does nothing and may be removed, might be useful if we ever start hosting events in a noSQL database.
* Type: What type of event is this? Is it about Apple, then put "Apple". Is it about IBM? Then put "IBM". This deterimines the styling for the event. More documentation to come for this.
* A one sentence description of the event. Used for the event in the initial timeline.
* Body: The actual text describing the event. This can be as long as you want it, just make sure it's within the quoted strings on the line.
* Date: When the event happened, either a string or a number, since problems exist with the DATE Javascript notation.
* Location: Where the event happened
* Citations: Put any citations here? If there are none, that's fine (at least on a code level, as a amateur historian, it's bad).
* TimelineImage: The image shown during the initial timeline
* EventFocusImages: The image(s) shown in the body of the EventInFocus. None are necessary, though at leas one is preferred.

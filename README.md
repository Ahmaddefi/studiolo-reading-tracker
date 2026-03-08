The Studiolo — Personal Reading Tracker
A beautiful, fully offline reading tracker built as a single HTML file. No installation, no account, no internet connection required after download. Open it in any browser and it works.
Built for serious readers running a long-term intellectual reading programme across multiple disciplines.

Load image

What It Is
Most reading trackers are built for casual readers. This one is built for people running a structured, multi-year reading programme who want to track not just what they read but why they read it in a particular order.
The app ships with a pre-loaded curriculum across three tracks:
African History — 26 books across 6 stages, from the precolonial foundations through the slave trade, colonialism, and the postcolonial present
Western Philosophy — 16 books sequenced from orientation texts through the primary sources and into the twentieth century
Literature & The Western Canon — 88 books across 11 stages, pairing African and postcolonial fiction with the history track, and covering the full arc of Western literature from Homer to Cormac McCarthy, including essential essays in personal, political, and literary criticism
130 books total. Designed to be read over 5 to 7 years.
You do not have to use this curriculum. The structure is built to hold any reading programme you design.

Features
Dashboard
Overall completion percentage across all tracks
Per-track progress bars
Day streak counter
Rotating quotes from authors on the reading list
"You Are Here" panel showing the next book on each track
Three Track Panels
Books organised by stage, in reading order
Each book card shows title, author, reading stage, and pairing notes (which books connect to which)
Status toggle: Not Started / Reading / Finished
Five-star rating that appears after marking a book finished
Collapsible notes field per book for your own thoughts
Accountability Map
A linear timeline of every book across every track
Finished books recede into shadow
Current book glows amber
Next unread book is marked "You Are Here"
The map asks one question clearly: what have you done, and what remains?
Reading Journal
Dated free-text entries
Write after difficult chapters, after books that changed something, after anything that needs processing
All entries saved and accessible from the sidebar
Writing a journal entry counts toward your reading streak
Persistence

Everything is saved in your browser's local storage
Close the tab, come back in a year, nothing is lost
No account required, no server, no data leaves your machine

How to Use It
Click the green Code button on this page
Click Download ZIP
Unzip the file
Open studiolo-reading-tracker.html in any browser (Chrome, Firefox, Safari, Edge all work)
That is it
Or click directly on the file above, then click the Download raw file button (the down arrow icon in the top right of the file view).

Customising the Reading List
The book data lives in a single JavaScript object near the top of the <script> tag, starting with const BOOKS = {. Each track is an array of stages, each stage is an array of books.
To add a book:
{ id: "ah27", title: "Your Book Title", author: "Author Name", pairs: "Pairs with Another Book" }
Keep the id unique. Use null for pairs if there is no pairing.
To add a stage to an existing track:
{
  stage: "Your Stage Name",
  books: [
    { id: "ah27", title: "Book One", author: "Author", pairs: null },
    { id: "ah28", title: "Book Two", author: "Author", pairs: null },
  ]
},

To create an entirely new track, add a new key to the BOOKS object, add a new panel to the HTML, wire it into the nav tabs, and add it to refreshAll(). The existing tracks show the pattern.

Design
The aesthetic is deliberate. Dark charcoal and near-black backgrounds, gold and amber accents, Cormorant Garamond and Crimson Pro typefaces, a subtle grain texture. It is meant to feel like a scholar's private study rather than a productivity dashboard. The environment you read in changes how you read. The environment you track in changes how you track.
No frameworks. No external dependencies except Google Fonts. Pure HTML, CSS, and JavaScript in one file. Fully mobile responsive.

The Story Behind This
I built this because I could not find a tool that took reading as seriously as I wanted to take it.
The problem was not motivation. The problem was structure. Reading without a curriculum is like building a house by buying materials in random order. You end up with a pile of interesting things that do not add up to anything.
I spent time designing a proper curriculum first — three disciplines, sequenced deliberately, with books paired across tracks so the fiction illuminates the history and the philosophy illuminates both. Then I built a tool that could hold it.
The full story is in this Medium article (https://medium.com/@TheAhmadkabir/i-designed-my-own-intellectual-curriculum-at-21-955cdfce4867).
Who This Is For
Serious readers who want more than a list
Anyone running or planning a multi-year reading programme
People who find that tracking progress and writing brief notes changes how deeply they engage with books
Anyone who wants a reading environment that feels considered rather than generic
Contributing
This is a personal project shared publicly. If you find a bug, open an issue. If you want to suggest a book for the default curriculum, open an issue with your reasoning. Pull requests for bug fixes are welcome.

Licence
MIT. Use it, adapt it, share it. If you build something from it, a mention would be appreciated but is not required.
Built by Muhammadkabir Yaqub — product manager, reader, thinker.

# circle_of_knowledge
In-depth learning materials implementing chart-based hierarchical data management

// Initial Skeleton //
circle_of_knowledge/
├── README.md
├── .gitignore
├── package.json
├── vite.config.ts
├── tsconfig.json
├── index.html
├── public/
│   ├── manifest.webmanifest        # makes it installable later
│   └── icons/
├── data/
│   ├── terms.json                  # every term: id, name, parentId, definition, level, tags
│   ├── links.json                  # connections: source, target, type
│   └── categories.json             # top-level branches + colors
├── scripts/
│   └── validate.ts                 # checks every parentId and link target exists
├── src/
│   ├── main.ts                     # entry point
│   ├── models/
│   │   └── types.ts                # Term, Link, LinkType, Level, Category
│   ├── store/
│   │   └── dataStore.ts            # terms + selection + search/filter state
│   ├── services/
│   │   ├── loadData.ts             # fetch/parse JSON
│   │   └── storage.ts              # localStorage / IndexedDB (favorites, progress)
│   ├── charts/
│   │   ├── SunburstChart.ts        # circular hierarchy (main view)
│   │   ├── TreeChart.ts            # category → subcategory → term
│   │   ├── NetworkChart.ts         # cross-links between terms
│   │   ├── LevelChart.ts           # term counts per category/level
│   │   └── index.ts                # exports all charts
│   ├── components/
│   │   ├── Sidebar.ts
│   │   ├── DetailPanel.ts          # definition + links of selected term
│   │   ├── SearchBar.ts
│   │   └── FilterBar.ts
│   ├── utils/
│   │   └── helpers.ts              # flat list → tree, sorting, etc.
│   └── styles/
│       └── main.css
└── docs/
    └── concepts.md                 # your learning notes
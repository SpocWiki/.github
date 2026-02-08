# Welcome to SpocWiki

### Building the Framework for universal, personal Knowledge-Webs.

SpocWiki is a collaborative initiative to provide high-quality, shared public **Wiki-Data**. 

We bridge the gap between massive research platforms like Wikipedia 
and the need for structured, private, and maintainable personal knowledge bases.

Whether you are using [Obsidian](https://obsidian.md/), [TiddlyWiki](https://de.wikipedia.org/wiki/TiddlyWiki), or a custom system, 
SpocWiki provides the modular building blocks — from geography to the sciences — 
to jumpstart your own "[Memex](https://en.wikipedia.org/wiki/Memex)."

---

## 🚀 Why SpocWiki?

While Wikipedia is an incredible resource, integrating it into a personal vault is often difficult 
due to rigid standards, consensus delays, and privacy needs. 

**SpocWiki exists to give you the best of both worlds:**

- **Platform-Agnostic:** Built primarily in Markdown with YAML frontmatter.
- **Modular Growth:** A "plug-and-play" repository structure. Don't need all of Europe? Just grab the countries or states you care about.
- **Data-Rich:** Includes `.svg`, `.png`, `.geoJson`, and `.csv` files for a visual and analytical experience.
- **Structured Freedom:** Optimized for Obsidian but designed to work with any Markdown-based Tool.

---

## 🌳 The  `_Standards` Repository

Everything we do is governed by our primary repository: 👉 **[SpocWiki/_Standards](https://github.com/SpocWiki/_Standards)**

This repository contains the global metadata, best practices, and semantic vocabularies 
that ensure all SpocWiki repositories remain interoperable and extensible.

You can retrieve additional, nested Repositories 
by clicking convenient Shell Commands in the corresponding Folders. 

See the full [[#🌿Repository Tree Structure]] 

---

## 🗺️ How it Works: Breadth over Depth

We focus on providing **factual, unbiased Reference-Data**. 
To keep performance high on mobile devices, we use a recursive sub-repository system:
1. **`_Standards`:** Covers high-level concepts and country-level stubs.
2. **Regional Repos:** (e.g., `Europe-Germany`) Provide deeper national data.
3. **Local Repos:** (e.g., `Germany-Bayern`) Provide granular regional details.
    

> [!TIP]
> 
> To expand your knowledge-web, simply clone a detail repository 
> into a folder named after the corresponding stub article in your parent vault! 
> 
> There are batch-Files  you can simply double-click to retrieve each sub-repository. 

---

## 🛠️ Our Conventions

To ensure our data never breaks, we adhere to some conventions in File-Names :
- **No Spaces:** We prefer `Kebab-Case` and `Snake_Case` to prevent URL escaping issues.
	- Wherever possibly we use the Name of the corresponding Wikipedia Article. 
	- We adhere to the Wikipedia conventions to 
		- avoid these characters `#`, `{`, `}`, `[`, `]`, and `|` 
		- omit Articles starting with "The"
- **Unique Names:** We avoid duplicate filenames to ensure clear linking across disjoint repositories 
	- except for the conventional ReadMe.md at each Repository Root.
	- Use a common Character Set
	- Disambiguation can be achieved in multiple ways: 
		- Append a qualifier, separated by Comma like `London,Ontario` 
		- Append a qualifier in Parentheses like `Mercury(Planet)`
		- Prepend the Parent Category, separated by Tilde like `Database~Schema` 
	- No `primary Topic`: each of the Documents with the same name must be disambiguated. 
		- This reduces the likelihood of wrong links 
	- Use `aliases:` in the FrontMatter YAML to improve Searching and provide all ambiguous Matches 
		- Duplicates in Aliases are encouraged (in reasonable amount). 
		- Spaces and otherwise disallowed characters are allowed in Aliases 
		- Multi-lingual Aliases in any script are encouraged to improve discoverability
    - Central Renames: Renaming can only be done centrally, because all Links need to be updated.
        - this can only be ensured by handling all Sub-Repositories consistently, which only few Users do. 
- **Semantic Data:** We use common, readable YAML attributes like `has_time_started` and `aliases` to make data queryable.
    

---

## 🤝 Join the Mission

SpocWiki is a shared resource. We welcome Pull Requests that improve data accuracy or expand our coverage.

- **Contribute:** Please read our [Contributing Guidelines](https://www.google.com/search?q=https://github.com/SpocWiki/_Standards/blob/main/Contributing.md) first.
    
- **License:** Our content is compatible with Wikipedia/Wikidata (CC BY-SA) to ensure free exchange of information. See [License](https://www.google.com/search?q=https://github.com/SpocWiki/_Standards/blob/main/License.md).
    
- **Storage:** Large media files are kept in the `xLarge` repository to keep your local clones lean.
    

**Ready to start?** Explore the **[\_Standards](https://github.com/SpocWiki/_Standards)** Repository and begin building your knowledge-web today.


## 🌿Repository Tree Structure  

This is the intended Nesting Structure of the current Repositories when all are retrieved. 
We recommend to retrieve only those needed, because e.g. Obsidian can handle only ca. 30_000 Files. 
All Leaf Folders (non-bracketed) are Repositories

```
└── _Standards
    ├── WikiData
    ├──(Astronomy)
    │   └──(Star)
    │       └── Stars
    ├──(bio)
    │   └──(bio~Domain)
    │       └──(Eukarya)
    │           └──(Animal)
    │               └──(Bilateria)
    │                   ├──(Arthropoda)
    │                   │   └──(Hexapoda)
    │                   │       └──(Insect)
    │                   │           └── Pterygota
    │                   └──(Deutero)
    │                       └──(Chordata)
    │                           └──(Craniata)
    │                               └──(Vertebrata)
    │                                   └──(Gnath)
    │                                       ├── Actinopterygii
    │                                       └──(Sarc)
    │                                           └──(Tetrapods)
    │                                               └──(Bird)
    │                                                   └── Neornithes
    └──(Earth)
        └──(Continent)
            ├── Oceania
            ├──(Africa)
            │   ├──(Africa~Central)
            │   │   ├── Burundi
            │   │   ├── Cameroon
            │   │   ├── Central_African_Rep
            │   │   ├── Chad
            │   │   ├── Congo~Brazzaville
            │   │   ├── Congo~Kinshasa
            │   │   ├── Equatorial_Guinea
            │   │   ├── Gabon
            │   │   ├── Niger
            │   │   ├── Nigeria
            │   │   ├── Rwanda
            │   │   ├── Sao_Tome_and_Principe
            │   │   ├── Uganda
            │   │   └── Zambia
            │   ├──(Africa~East)
            │   │   ├── British_Indian_Ocean_Territory
            │   │   ├── Comoros
            │   │   ├── Djibouti
            │   │   ├── Eritrea
            │   │   ├── Ethiopia
            │   │   ├── Kenya
            │   │   ├── Madagascar
            │   │   ├── Malawi
            │   │   ├──(Mascarene-Islands)
            │   │   │   ├── Mauritius
            │   │   │   └── Reunion
            │   │   ├── Mayotte
            │   │   ├── Mozambique
            │   │   ├── Seychelles
            │   │   ├── Somalia
            │   │   ├── Somaliland
            │   │   ├──(Sudan)
            │   │   │   ├── Sudan~North
            │   │   │   └── Sudan~South
            │   │   └── Tanzania
            │   ├──(Africa~North)
            │   │   ├── Algeria
            │   │   ├── Egypt
            │   │   ├── Libya
            │   │   ├── Morocco
            │   │   └── Tunisia
            │   ├──(Africa~South)
            │   │   ├── Angola
            │   │   ├── Botswana
            │   │   ├── Lesotho
            │   │   ├── Namibia
            │   │   ├── South_Africa
            │   │   ├── Swaziland
            │   │   └── Zimbabwe
            │   └──(Africa~West)
            │       ├── Benin
            │       ├── Burkina_Faso
            │       ├── Cape_Verde
            │       ├── Cote_d'ivoire
            │       ├── Gambia
            │       ├── Ghana
            │       ├── Guinea
            │       ├── Guinea-Bissau
            │       ├── Liberia
            │       ├── Mali
            │       ├── Mauritania
            │       ├── Senegal
            │       ├── Sierra_Leone
            │       ├── Togo
            │       ├── Tristan_da_Cunha-Islands
            │       └── Western_Sahara
            ├── America~Caribbean
            ├──(America~Central)
            │   ├── Belize
            │   ├── Costa_Rica
            │   ├── El_Salvador
            │   ├── Guatemala
            │   ├── Honduras
            │   ├── Mexico
            │   ├── Nicaragua
            │   └── Panama
            ├──(America~North)
            │   ├── Canada
            │   ├── Saint-Pierre-et-Miquelon
            │   └──(USA)
            │       ├── USA~5-Eastern
            │       ├── USA~6-Central
            │       ├── USA~7-Mountain
            │       └── USA~8-Pacific
            ├──(America~South)
            │   ├──(Andes)
            │   │   ├── Bolivia
            │   │   ├── Colombia
            │   │   ├── Ecuador
            │   │   ├── Peru
            │   │   └── Venezuela
            │   ├── Brazil
            │   ├── Falkland~Islands
            │   ├──(Guianas)
            │   │   ├── French_Guiana
            │   │   ├── Guyana
            │   │   └── Suriname
            │   └──(Southern_Cone)
            │       ├── Argentina
            │       ├── Chile
            │       ├── Paraguay
            │       └── Uruguay
            ├── Antarctica
            ├──(Australasia)
            │   ├── Australia
            │   ├── New_Caledonia
            │   └── New_Zealand
            ├──(Europe
            │   ├──(Europe~Central)
            │   │   ├── Austria
            │   │   ├── Croatia
            │   │   ├── Czech_Republic
            │   │   ├── Germany
            │   │   ├── Liechtenstein
            │   │   ├── Slovakia
            │   │   ├── Slovenia
            │   │   └── Switzerland
            │   ├──(Europe~East)
            │   │   ├── Belarus
            │   │   ├── Bulgaria
            │   │   ├── Georgia,Europe
            │   │   ├── Hungary
            │   │   ├── Moldova
            │   │   ├── Poland
            │   │   ├── Romania
            │   │   ├── Russia
            │   │   ├── Turkey
            │   │   └── Ukraine
            │   ├──(Europe~North)
            │   │   ├── Denmark
            │   │   ├── Estonia
            │   │   ├── Finland
            │   │   ├── Greenland
            │   │   ├── Iceland
            │   │   ├── Ireland
            │   │   ├── Latvia
            │   │   ├── Lithuania
            │   │   ├── Norway
            │   │   ├── Sweden
            │   │   └── UK
            │   ├──(Europe~South)
            │   │   ├── Albania
            │   │   ├── Andorra
            │   │   ├── Bosnia-Herzegovina
            │   │   ├── Cyprus
            │   │   ├── Greece
            │   │   ├── Italy
            │   │   ├── Kosovo
            │   │   ├── Macedonia~North
            │   │   ├── Malta
            │   │   ├── Montenegro
            │   │   ├── Portugal
            │   │   ├── San_Marino
            │   │   ├── Serbia
            │   │   └── Spain
            │   └──(Europe~West)
            │       ├── Belgium
            │       ├── France
            │       ├── Luxembourg
            │       ├── Monaco
            │       └── Netherlands
            └──(Asia
                ├──(Asia~Central)
                │   ├── Afghanistan
                │   ├── Kazakhstan
                │   ├── Kyrgyzstan
                │   ├── Tajikistan
                │   ├── Turkmenistan
                │   └── Uzbekistan
                ├──(Asia~East)
                │   ├── China
                │   ├── Japan
                │   ├──(Korean_Peninsula
                │   │   ├── Korea~North
                │   │   └── Korea~South
                │   ├── Mongolia
                │   └── Taiwan
                ├── Asia~North
                ├──(Asia~North~West)
                │   ├── Armenia
                │   └── Azerbaijan
                ├──(Asia~South~East)
                │   ├── Cambodia
                │   ├── Laos
                │   ├──(Malay_Archipelago)
                │   │   ├── Indonesia
                │   │   ├── Malaysia
                │   │   ├── Papua-New_Guinea
                │   │   ├── Philippines
                │   │   ├── Singapore
                │   |   └──(Timor)
                │   |       └── Timor-Leste
                │   ├── Myanmar
                │   ├── Thailand
                │   └── Vietnam
                ├──(Asia~West)
                │   ├── Bahrain
                │   ├── Iran
                │   ├── Iraq
                │   ├── Israel
                │   ├── Jordan
                │   ├── Kuwait
                │   ├── Lebanon
                │   ├── Oman
                │   ├── Qatar
                │   ├── Saudi_Arabia
                │   ├── Syria
                │   ├── United_Arab_Emirates
                │   └── Yemen~Republic
                └──(Indian_Subcontinent)
                    ├── Bangladesh
                    ├── Bhutan
                    ├── India
                    ├── Maldives
                    ├── Nepal
                    ├── Pakistan
                    └── Sri_Lanka
```


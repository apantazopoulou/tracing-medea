# Tracing Medea

## Documentation: Instructions

See `readme_instructions.md` in the repository for instructions on editing and adding basic content files.

## Next Steps: Site Content
1. **Build out content**. Create play content pages following instructions provided by Wiebke Kuhn and Sam Munch in `readme_instructions.md`.
2. **Update play metadata** following the template and examples in `_data/play-demo-metadata.csv`. Use file name "play-demo-metadata.csv" for new csv files to avoid changing the website datasource.
3. **Add photos** to `/assests/img/` directory. If image should be included in a map popup, make sure to update the .csv file with the file name and extension and file type following the model provided.

## Next Steps: Site Coding & Architecture
Suggested by Stella Fritzell (GitHub: sfritzell) following work at 2024 ILiADS:

1. **Create page layout template** for markdown content with embeded map: A non-functioning possibility can be found at `_layouts/page-map.html` in Stella's forked repository (`sfritzell/tracing-medea`)
2. **Standardize metadata CSV** to follow template established in `_data/play-demo-metadata.csv`. New fields can be added, but caution should be observed with field names (refer to [Collection Builder documentation](https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/). Use file name "play-demo-metadata.csv" for new csv files to avoid changing the website datasource. If changing the file name, update in `_config.yml`.
3. **Fix image thumnail display** in map popups. This likely an issue with the `_includes/js/map-js.html` and / or the `_data/play-demo-metadata.csv` files and referenced file paths. Code currently appears to be recognizing file path and type for the stored images, but is failing to reference the image itself. Collection Builder site code should already be scaling the image correctly regardless of file type (jpeg, sgv, etc), so this is probably not the issue.
4. **Create map subject layers**. Should occur in `_includes/js/map-js.html file`. Should be possible with `L.layerGroup()` and using something like `feature.properties.subject.includes("dictonary value")` as a filter.
5. **Set regional map focus** on region pages. Dependent on item 1 (page layout template) and assigning template in yaml header for each regional landing page. There is a Collection Builder discussion on [filtering a map](https://github.com/orgs/CollectionBuilder/discussions/104) for different pages that would be a good starting point.

---

# About CollectionBuilder-GH

A project to generate a free and simple digital collection site using [GitHub Pages](https://pages.github.com/) given:

- a CSV of collection metadata
- a folder of JPEG images, PDF documents, MP3s, or links to videos hosted on YouTube or Vimeo

Visit the [demo site](https://collectionbuilder.github.io/collectionbuilder-gh/).

## Build a Digital Collection

Gather your digital objects together and create your metadata using the [CollectionBuilder-GH Metadata Template](https://docs.google.com/spreadsheets/d/1Uv9ytll0hysMOH1j-VL1lZx6PWvc1zf3L35sK_4IuzI/copy) and [metadata docs](https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/). 

Then click the green "use this template" button to create your repository, and add your metadata and configure the repository to fit your collection and settings following the [CollectionBuilder Docs](https://collectionbuilder.github.io/cb-docs/). 

Please feel free to ask questions in the main [CollectionBuilder discussion forum](https://github.com/CollectionBuilder/collectionbuilder.github.io/discussions).

**Note:** 
Since CollectionBuilder-GH uses [GitHub Pages](https://pages.github.com/), it is only suitable for small collections, with lower resolution images. 
GitHub repositories are limited to 1GB.
For larger collections or those that require more customization, check out the [CollectionBuilder-CSV](https://github.com/CollectionBuilder/collectionbuilder-csv) template.

## CollectionBuilder-GH Quick Tutorial

Follow the [CollectionBuilder-GH Walkthrough](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/gh-walkthrough/) to set up a collection quickly using demo metadata and objects. 

- [Demo Metadata](https://docs.google.com/spreadsheets/d/1x48Te3duPAxh53foEihQVKTfCKUjaCCbH7TrMMd_yU4/copy)
- [Demo Objects](https://www.lib.uidaho.edu/collectionbuilder/demo-objects.zip)

## Teaching and Learning with CollectionBuilder-GH

CollectionBuilder-GH is intended as a simple template for hands-on teaching about digital libraries.
It can be used in a workshop setting to take participants through digitization and metadata creation, to having a live collection site hosted on GitHub.

CollectionBuilder-GH aims to be well documented and easy to configure by following the documentation, with the potential to scaffold learning of a multitude of transferable digital and data skills.
A project in "minimal computing", it provides a depth of learning opportunities, allowing users to take complete ownership over the project and make their work open to the world.

Learn about:

- Git and GitHub basics
- [Markdown](https://guides.github.com/features/mastering-markdown/), plaintext writing and content creation
- HTML, CSS, and JavaScript literacy
- command line literacy
- GitHub collaboration and project management
- [Jekyll](https://jekyllrb.com/) basics
- working in the Open, open source and open data
- digital libraries concepts such as "collections as data", minimal computing, data-driven design

> We prefer commonly understood formats (such as CSV spreadsheets over YAML), and convention over configuration (follow the example over learn all the options).

----------

## CollectionBuilder 

<https://collectionbuilder.github.io/>

CollectionBuilder is a project of University of Idaho Library's [Digital Initiatives](https://www.lib.uidaho.edu/digital/) and the [Center for Digital Inquiry and Learning](https://cdil.lib.uidaho.edu) (CDIL) following the [Lib-Static](https://lib-static.github.io/) methodology. 
Powered by the open source static site generator [Jekyll](https://jekyllrb.com/) and a modern static web stack, it puts collection metadata to work building beautiful sites.

The basic theme is created using [Bootstrap](https://getbootstrap.com/).
Metadata visualizations are built using open source libraries such as [DataTables](https://datatables.net/), [Leafletjs](http://leafletjs.com/), [Spotlight gallery](https://github.com/nextapps-de/spotlight), [lazysizes](https://github.com/aFarkas/lazysizes), and [Lunr.js](https://lunrjs.com/).
Object metadata is exposed using [Schema.org](http://schema.org) and [Open Graph protocol](http://ogp.me/) standards.

Questions can be directed to **collectionbuilder.team@gmail.com**

## License

CollectionBuilder documentation and general web content is licensed [Creative Commons Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/). 
This license does *NOT* include any objects or images used in digital collections, which may have individually applied licenses described by a "rights" field.
CollectionBuilder code is licensed [MIT](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/master/LICENSE). 
This license does not include external dependencies included in the `assets/lib` directory, which are covered by their individual licenses.

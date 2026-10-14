# Forest Ecosystem

Three connected projects, with a shared home for digital asset concepts on aelf.

## Navigate the ecosystem

### Forest — collections and items

Start at `/` to learn how NFT collections group related items, how symbols identify them, and how metadata describes their artwork and attributes. Forest also introduces the role of SEEDs in the wider ecosystem.

### Symbol Market — SEEDs and token names

Continue at `/symbolmarket/` for the relationship between a SEED and its associated symbol. These pages distinguish fungible token definitions, NFT collections, and individual items, and explain why the chain and full symbol matter when reading a record.

### aelf Inscriptions — definitions and supply

Visit `/aelfinscription/` to explore ticks, total supply, limits per mint, and the terminology used in inscription records. Topic pages connect deployment, issuance, and minting concepts with public project references.

## How the repository is organised

```text
index.html                 Forest home
assets/                    Forest artwork and Poppins fonts
symbolmarket/              Symbol Market pages, styles, and assets
aelfinscription/           Inscription pages, styles, and assets
static-manifest.json       Complete page and file inventory
source-provenance.json     Asset checksums and Forest source reference
```

Each project keeps its visual identity and resource directory. The shared navigation connects the three home pages; topic pages remain within their project's directory.

## Developing and hosting

Start a preview from the repository root:

```sh
python3 -m http.server 4178 --bind 127.0.0.1
```

Browse [Forest](http://127.0.0.1:4178/), [Symbol Market](http://127.0.0.1:4178/symbolmarket/), or [aelf Inscriptions](http://127.0.0.1:4178/aelfinscription/).

Deploy the full directory at the root of a domain. The three sites share root-relative navigation, so a GitHub Pages custom domain provides the expected URL layout. The host should support directory indexes and return HTTP 404 for unknown addresses.

Forest and both companion projects include their own `404.html` content. Error-page selection and status codes are configured by the host.

## Project references

The [eforest-finance organisation](https://github.com/eforest-finance) contains the [contracts](https://github.com/eforest-finance/forest-contract), [interface](https://github.com/eforest-finance/forest-interface), and [server](https://github.com/eforest-finance/forest-server) repositories.

[aelf documentation](https://docs.aelf.com/) provides chain context, [AElfScan](https://aelfscan.io/) provides public blockchain records, and [aelf.com](https://aelf.com/) introduces the network.

Forest's artwork and Poppins fonts originate from the Forest interface repository. Symbol Market and aelf Inscriptions keep their artwork and fonts alongside their pages. Asset references are recorded in `source-provenance.json`.

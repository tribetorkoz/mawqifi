<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg">
  <img src="./assets/banner-dark.svg" alt="Mawqifi banner" width="100%">
</picture>

<br>

<img src="https://img.shields.io/badge/JavaScript-161B22?style=flat-square&labelColor=0D1117&logo=javascript&logoColor=A855F7" alt="JavaScript">
<img src="https://img.shields.io/badge/PWA-161B22?style=flat-square&labelColor=0D1117&logo=pwa&logoColor=A855F7" alt="PWA">
<img src="https://img.shields.io/badge/Vercel-161B22?style=flat-square&labelColor=0D1117&logo=vercel&logoColor=A855F7" alt="Vercel">
<img src="https://img.shields.io/badge/Arabic-161B22?style=flat-square&labelColor=0D1117&logo=googletranslate&logoColor=A855F7" alt="Arabic">

<br><br>

<a href="#quick-start">Quick Start</a> · <a href="#features">Features</a>

</div>

## Overview

Commuting in an unfamiliar city is a sequence of small uncertainties: is this GPS reading trustworthy, which stop is actually nearest, how long is the walk, when does the bus come. **Mawqifi** answers those in one Arabic-language surface, and deliberately rejects stale or outlier GPS readings instead of routing from bad data.

> **Deployment note:** the v8 build is not currently live. The earlier v5 build remains archived at [`256`](https://github.com/tribetorkoz/256) and is still served at [256-six.vercel.app](https://256-six.vercel.app).

## Features

| | |
|---|---|
| **GPS quality gating** | Scores fix accuracy and refuses stale or outlier readings |
| **Nearest stop** | Ranks stops by real walking distance, not straight-line distance |
| **Walk time only** | Shows minutes of walking without inventing arrival clock times |
| **Bus ETA** | Estimates the next departure from the published morning schedule |

## Stack

Vanilla JavaScript · HTML/CSS · Service Worker · Vercel static hosting

## Quick Start

```bash
git clone https://github.com/tribetorkoz/mawqifi.git
cd mawqifi
npx vercel --prod     # or serve public/ with any static server
```


## License

MIT

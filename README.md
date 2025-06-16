# 🇮🇩 Indonesia Data API (via GitHub Pages)

This repository provides structured data regarding Indonesia, hosted as a **static JSON API** using **GitHub Pages**.

💡 _This is part of my self-study realization. The idea is not original and many people already have similar repository like this._

> 📍 **Current available dataset:** Region data consisting of **provinces to villages**.
> ✅ Simple, fast, and publicly accessible — no authentication needed.

---

## 📦 What’s Inside

This repository currently includes:

- **Provinces** (`region/provinces.json`)
- **Cities / Regencies** (`region/cities/`)
- **Districts / Subdistricts** (`region/districts/`)
- **Villages** (`region/villages/`)

Each dataset is structured and standardized in a unified JSON format, including:

```json
{
  "code": 200,
  "status": "OK",
  "message": "Request has been successfully processed.",
  "data": [ /* Region-specific data */ ],
  "metadata": {
    "totalRow": 1
  }
}
```

---

## 🌐 How to Use

You can fetch data directly using HTTP `GET` requests:

```bash
curl https://jeremygprawira.github.io/indonesia/region/provinces.json
```

Or for a specific city, for example:

```bash
curl https://jeremygprawira.github.io/indonesia/region/cities/11.json
```

Or for a specific district, for example:

```bash
curl https://jeremygprawira.github.io/indonesia/region/districts/11.01.json
```

Or for a specific village, for example:

```bash
curl https://jeremygprawira.github.io/indonesia/region/villages/11.01.01.json
```

---

## 🕒 Timezone Info

Each data point includes timezone metadata:

```json
"indonesiaTimezone": "WIB",
"ianaTimezone": "Asia/Jakarta",
"timezoneOffset": "+07:00"
```

---

## 📌 Example Use Cases

- Location auto-fill or cascade dropdowns
- Offline-ready reference for Indonesian administrative areas
- Mapping or visualization tools
- Regional analytics based on postal codes or boundaries

---

## 🛠️ Format & Structure

Each file in the dataset maintains a consistent structure:
- `type`: region level (e.g., `province`, `city`, `district`, `village`)
- `code`: unique standardized code
- `name`: region name (uppercase)
- `provinceCode`, `cityCode`, etc.: hierarchical references
- Additional metadata (postal code, coordinates, timezone)

---

## ⚠️ GitHub Pages Bandwidth & Build Limits

When using **GitHub Pages** to host static content like JSON APIs for provinces, cities, districts, and villages, be aware of the following limitations:

---

### 🔸 Bandwidth Limit

- GitHub Pages has a **soft bandwidth limit of 100 GB per month**.
- This includes **all traffic** to your static files (e.g., JSON, HTML, JS, images).
- If your usage exceeds this limit, GitHub may **throttle or temporarily disable your site**.
- Public APIs or datasets accessed frequently can **quickly exhaust this quota**.

---

### 🔸 Build Limit

- GitHub Pages enforces a **soft limit of 10 builds per hour**.
- Every time you push changes to the branch used for GitHub Pages (e.g., `main` or `gh-pages`), a **build is triggered**.
- Too many commits or automated updates can **delay deployments** if the limit is hit.

---

## 🛣️ Roadmap

- [x] Manual population of regional data from provinces to villages
- [ ] Create automated scripts to scrape or fetch the latest regional data from official sources
- [ ] Add versioning support for datasets
- [ ] Add more datasets (e.g. population, economic, geographic)
- [ ] Build interactive documentation (Swagger-like view or a simple website)
- [ ] Add multi-language support (e.g. English, Indonesian)

💡 _Currently, the data is collected manually from various official sources. In the future, this will be automated via custom scripts._

---

## 📄 License

This dataset is provided as-is for public use. Attribution is appreciated but not required. Data sources are based on standardized government region codes (Kemendagri) and publicly available resources.

---

## 🙏 Contributing

Have suggestions, corrections, or want to help us grow the dataset?

> Pull requests and issues are welcome!

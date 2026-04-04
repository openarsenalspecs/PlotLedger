# PlotLedger Workflow

**PlotLedger** — *The Future of Parcel Intelligence*  
Created by **Roxanne Ardary** | [roxanneardary.com](https://www.roxanneardary.com/)

This workflow outlines the recommended process for contributing to, maintaining, and using the PlotLedger repository, ensuring consistency, data integrity, and proper attribution.

---

## 1. Repository Structure

- `data/` — Contains raw and processed parcel, zoning, and permit data files.
- `scripts/` — Data ingestion, parsing, and AI analysis scripts.
- `frontend/` — Map visualization and user interface files (React / Mapbox / Leaflet).
- `backend/` — API, database integration, and server scripts.
- `docs/` — Documentation files, including this Workflow.md.
- `LICENSE` — AGPL-3.0+ license file.
- `notice.md` — Attribution and usage notice.
- `README.md` — Project overview and setup instructions.

---

## 2. Development Workflow

### 2.1 Branching

- **main** — Stable release branch.
- **dev** — Active development branch; all new features and fixes should be merged here first.
- **feature/[name]** — Feature-specific branches created from `dev`.
- **hotfix/[name]** — Urgent fixes created from `main`.

### 2.2 Commit Guidelines

- Use **clear, descriptive commit messages**.
- Include issue or feature references where applicable.
- Maintain consistency with existing code formatting and documentation.

---

## 3. Data Management

1. **Ingestion**
   - Use scripts in `scripts/ingest` to load parcel and zoning data.
   - Ensure all datasets are validated and cleaned before merging.

2. **Processing**
   - Merge contiguous parcels ≥9 acres.
   - Normalize ownership names and sale history records.
   - Cross-reference permits and zoning laws.

3. **AI Analysis**
   - Run scripts to:
     - Detect special privileges or variances.
     - Score parcels for development potential.
     - Predict permit outcomes.

4. **Storage**
   - Use PostGIS / PostgreSQL to store spatial and relational data.
   - Maintain backups for all state-level datasets.

---

## 4. Frontend & Visualization

- Use Mapbox or Leaflet to display parcels interactively.
- Color-code parcels based on:
  - Privilege tiers
  - Zoning classifications
  - Development potential scores
- Enable filters for state, county, owner, parcel size, and permit status.
- Export reports and datasets as needed.

---

## 5. Contribution Guidelines

- Fork the repository and create a **feature branch** for your work.
- Test all scripts and visualizations locally before submitting a pull request.
- Include **attribution to Roxanne Ardary** and [roxanneardary.com](https://www.roxanneardary.com/) for any added code or datasets.
- Ensure all additions comply with the **AGPL-3.0+ license**.

---

## 6. Deployment & Updates

1. Update datasets regularly from county GIS, permit, and zoning portals.
2. Re-run AI analysis after data updates.
3. Merge changes into `dev` for testing; then into `main` for stable release.
4. Tag releases with semantic versioning (v[major].[minor].[patch]).

---

## 7. License & Attribution

All project code, data processing scripts, and documentation are licensed under **GNU Affero General Public License v3.0+ (AGPL-3.0+)**.  
Attribution must always be given to **Roxanne Ardary** and [roxanneardary.com](https://www.roxanneardary.com/).

---

**PlotLedger** — *The Future of Parcel Intelligence.*
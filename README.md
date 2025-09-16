# Bank-loan-analysis-PowerBI

<!-- ────────────────────────────── -->
<!-- HERO / THUMBNAIL              -->
<!-- Replace banner.png with a     -->
<!-- wide screenshot (~1600 × 400) -->
<!-- ────────────────────────────── -->

<p align="center">
  <img src="assets/banner.png" alt="Bank-Loan Analytics Dashboard – Power BI"/>
</p>

<h1 align="center">Bank-Loan Analytics Dashboard 📊</h1>
<p align="center">
  Credit-risk insights & KPI storytelling in <strong>Power BI</strong><br/>
  Powered by the public <em>Lending Club</em> loan-origination dataset
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power&nbsp;BI-DAX&nbsp;•&nbsp;Power&nbsp;Query&nbsp;•&nbsp;Data&nbsp;Modelling-yellow?style=flat-square"/>
  <img src="https://img.shields.io/github/license/your-handle/bank-loan-dashboard?style=flat-square"/>
</p>

---

## ✨ Project Showcase

<table>
  <tr>
    <td align="center"><strong>Portfolio-ready visuals</strong></td>
    <td align="center"><strong>Good v Bad segmentation</strong></td>
    <td align="center"><strong>Interactive USA map</strong></td>
  </tr>
  <tr>
    <td><img src="assets/overview.gif" alt="Interactive overview GIF"/></td>
    <td><img src="assets/good_bad_pie.png" alt="Good vs Bad loan pie"/></td>
    <td><img src="assets/state_map.png"  alt="Loan distribution map"/></td>
  </tr>
</table>

> **Pro tip:** record a 5-second GIF (e.g. ScreenToGif) of you clicking slicers; save as `assets/overview.gif`.

---

## 📚 Business Context

The dashboard mirrors a typical credit-risk-analyst workflow:

1. **Monitor originations** – track loan count & funded volume across terms, grades, and purpose.  
2. **Flag deterioration** – spot spikes in *Bad Loan %* or DTI outliers with conditional formatting.  
3. **Benchmark segments** – compare interest-rate spreads by borrower grade and employment length.  
4. **Geo deep-dive** – use the map to surface at-risk states and drill down to county-level patterns.  

---

## 🔧 Data Pipeline & Architecture

```mermaid
graph LR
    A[📂 CSV<br/>Lending Club 2007-2020] -->|Power Query<br/>(data cleansing)| B[🗄️ Star Schema<br/>“financial_loan” fact]
    B --> C[🧮 DAX Measures<br/>Risk KPIs]
    C --> D[📊 Report Pages<br/>Overview & Deep-dive]

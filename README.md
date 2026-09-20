# ArabDeals Product Listing & Multi-Tier Filters — QA Evidence & Client Deliverables

Comprehensive Quality Assurance and Automated End-to-End (E2E) Test Evidence package for the **ArabDeals Product Listing Multi-Tier Hierarchical Filtering & UX Architecture** across both the **Seller/Vendor Dashboard** and the **Platform Admin Dashboard**.

---

## 📊 Executive Summary & Test Metrics

| Metric | Result |
|:---|:---|
| **E2E Automation Tool** | Playwright (Chromium Headless with Video & Screenshots) |
| **Total Test Scenarios** | 20 Scenarios Verified |
| **Pass Rate** | **100% PASS (20 / 20)** |
| **Bulk Ingested Catalog** | 150 Main Products (Series 1 – 150) |
| **Total Product Variants** | 600 Sub-Variants (3 to 5 variants per product) |
| **Brands Covered** | 12 Brands (Apple, Samsung, Anker, Porodo, Baseus, Powerology, Riversong, Heatz, Sony, Xiaomi, Huawei, Belkin) |
| **Categories Covered** | 10 Category Trees (3-Tier Hierarchies: Main > Sub > Sub-sub) |
| **Vendors Tested** | 4 Marketplace Vendors (TechZone LLC, Al-Baraka Tech, Muscat Mobile Hub, Sultanate Gadgets) |
| **Key Features Verified** | 3-Tier Category Drilldown, Brand Strip, Status Pills (Approval, Stock, Product), Sort By, Price Range, 1-Click Filter Reset, Admin Vendor Selector, Variant Inline Modal |

---

## 📂 Repository Contents & Deliverables

### 1. Spreadsheets for Client Sharing (Excel & Google Sheets)
- **[ArabDeals_Product_Filters_E2E_Test_Evidence.xlsx](ArabDeals_Product_Filters_E2E_Test_Evidence.xlsx)**:
  - Multi-tab Excel workbook containing:
    1. `Executive Summary`: Overall project KPIs and verification parameters.
    2. `E2E Test Results (20 Cases)`: Complete test execution matrix with Test IDs, Features, Actions, Expected Results, Actual Results, Status (`PASS`), and Evidence References.
    3. `Vendor Dashboard Tests`: Breakdown of the 14 seller dashboard test cases.
    4. `Admin Dashboard Tests`: Breakdown of the 6 admin dashboard test cases.
    5. `150 Products Sample Catalog`: Sample product records showing codes, SKUs, pricing, variants, and stock.
  - **Google Sheets Usage**: In [Google Sheets](https://sheets.google.com), go to **File > Import > Upload** and select this `.xlsx` file to instantly create an active Google Sheet.
- **[ArabDeals_Product_Filters_E2E_Test_Evidence.csv](ArabDeals_Product_Filters_E2E_Test_Evidence.csv)**:
  - Standard CSV export of all 20 test cases for instant 1-click import into Google Sheets.

### 2. Interactive Web Report
- **[index.html](index.html)**:
  - Interactive QA dashboard styled like Google Sheets with tabs, KPI cards, clickable screenshot modals, and embedded video players.

### 3. Downloadable ZIP Package
- **[ArabDeals_Product_Filters_QA_Evidence.zip](ArabDeals_Product_Filters_QA_Evidence.zip)**:
  - All-in-one downloadable archive containing the Excel spreadsheet, CSV, HTML report, all 20 screenshots, and video recordings.

### 4. Visual Evidence Folders
- **`screenshots/`**: 20 high-resolution screenshots covering each step of test execution.
- **`videos/`**: Playwright WebM screen recordings capturing complete interactions.

---

## 📸 Test Case Matrix & Evidence Screenshots

### Seller / Vendor Dashboard (14 Tests)

| ID | Feature | Scenario Description | Evidence Screenshot | Status |
|:---:|:---|:---|:---:|:---:|
| **TC-V01** | Table Columns & Layout | Default 150 products list view with pagination & 10 exact columns | [01_product_listing_default_view.png](screenshots/01_product_listing_default_view.png) | `PASS` |
| **TC-V02** | Category Hierarchy (L1) | Click Level 1 Main Category tab (`CHARGER & CABLE`); active red pill | [02_category_level1_charger_selected.png](screenshots/02_category_level1_charger_selected.png) | `PASS` |
| **TC-V03** | Category Hierarchy (L2) | Click Level 2 Subcategory link (`HOME ADAPTER`); red underline indicator | [03_category_level2_home_adapter_selected.png](screenshots/03_category_level2_home_adapter_selected.png) | `PASS` |
| **TC-V04** | Category Hierarchy (L3) | Click Level 3 Sub-subcategory link (`USB A & C HOME ADAPTER`); table filtered | [04_category_level3_usb_ac_selected.png](screenshots/04_category_level3_usb_ac_selected.png) | `PASS` |
| **TC-V05** | Brand Strip | Filter by brand (`PORODO`) from `Brands >` strip | [05_brand_porodo_selected.png](screenshots/05_brand_porodo_selected.png) | `PASS` |
| **TC-V06** | Approval Status | Filter by `UNDER REVIEW` status pill | [06_approval_under_review_filtered.png](screenshots/06_approval_under_review_filtered.png) | `PASS` |
| **TC-V07** | Stock Status | Filter by `LOW STOCK` (0 < stock < 10) status pill | [07_stock_status_low_stock_filtered.png](screenshots/07_stock_status_low_stock_filtered.png) | `PASS` |
| **TC-V08** | Product Status | Filter by `ACTIVE` listing status (`isBlocked: false`) | [08_product_status_active_filtered.png](screenshots/08_product_status_active_filtered.png) | `PASS` |
| **TC-V09** | Sort By | Sort products by `Price: Low to High` | [09_vendor_sort_price_asc.png](screenshots/09_vendor_sort_price_asc.png) | `PASS` |
| **TC-V10** | Price Range | Custom budget filter: Min 10, Max 100 OMR | [10_vendor_price_range_filtered.png](screenshots/10_vendor_price_range_filtered.png) | `PASS` |
| **TC-V11** | Search Keyword | Regex search for `Series` across name, SKU, code | [11_search_product_filtered.png](screenshots/11_search_product_filtered.png) | `PASS` |
| **TC-V12** | 1-Click Reset | Click `✕ Reset (N)` button; restores all 150 products | [12_vendor_reset_all_filters.png](screenshots/12_vendor_reset_all_filters.png) | `PASS` |
| **TC-V13** | Page Size & Pagination | Set page size to 20 and navigate to Page 2 | [13_vendor_pagination_page_size.png](screenshots/13_vendor_pagination_page_size.png) | `PASS` |
| **TC-V14** | Inline Variant Modal | Click stock edit pencil icon; opens variant modal | [14_variant_inline_edit_modal_opened.png](screenshots/14_variant_inline_edit_modal_opened.png) | `PASS` |

### Platform Admin Dashboard (6 Tests)

| ID | Feature | Scenario Description | Evidence Screenshot | Status |
|:---:|:---|:---|:---:|:---:|
| **TC-A01** | Admin Product Overview | Admin default listing with 150 bulk products & navigation | [15_admin_dashboard_product_listing.png](screenshots/15_admin_dashboard_product_listing.png) | `PASS` |
| **TC-A02** | Admin Vendor Filter | Filter products by specific vendor (`TechZone Electronics LLC`) | [16_admin_vendor_filtered.png](screenshots/16_admin_vendor_filtered.png) | `PASS` |
| **TC-A03** | Admin Brand & Status | Filter by brand `ANKER` and status `APPROVED` | [17_admin_brand_status_filtered.png](screenshots/17_admin_brand_status_filtered.png) | `PASS` |
| **TC-A04** | Admin Sort By | Sort products by `Price: High to Low` | [18_admin_sort_price_desc.png](screenshots/18_admin_sort_price_desc.png) | `PASS` |
| **TC-A05** | Admin Reset Filters | Click `✕ Reset` button; restores full 150 products | [19_admin_reset_filters.png](screenshots/19_admin_reset_filters.png) | `PASS` |
| **TC-A06** | Admin Multi-Page Nav | Navigate across pages (Page 3) through the 150-product catalog | [20_admin_pagination.png](screenshots/20_admin_pagination.png) | `PASS` |

---

## 🎥 Full Interaction Video Recordings
- **Seller / Vendor Dashboard Test Run**: [`videos/page@fff81e121c300e7c8f134cb896b61961.webm`](videos/page@fff81e121c300e7c8f134cb896b61961.webm)
- **Admin Dashboard Test Run**: [`videos/page@ea8b19c66066eb636f172cfc4ba2a589.webm`](videos/page@ea8b19c66066eb636f172cfc4ba2a589.webm)

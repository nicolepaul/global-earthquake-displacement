# Predicting population displacement due to earthquakes globally 🌏🌎🌍

This repository contains code to support a manuscript that is not yet published. The readme will be updated once peer review has been successfully completed.

> Nicole Paul, Vitor Silva, Jack Baker, Magdalena Peter, Robert Oakes, Sylvain Ponserre, and Carmine Galasso. Predicting population displacement due to earthquakes globally.

## Overview

This repository contains data, analysis code, and a dashboard app. The analysis code is embedded within the dashboard app

### Data

The **event-based impact data and corresponding covariates** are available at: [assets/data.csv](assets/data.csv).

The **global probabilistic risk results** are available at: 

* Average annual displacement, national ([assets/global_aad-0.csv](assets/global_aad-0.csv))

* Average annual displacement, subnational ([assets/global_aad-1.csv](assets/global_aad-1.csv))

* Probable maximum displacement ([assets/global_pmd.csv](assets/global_pmd.csv))

### Analysis

To replicate the analysis, it is recommended to run the dashboard locally.

By default, production mode is set to `True`, which improves performance at the cost of only using the ideal hyperparameter configuration. However, if you want to repeat the grid search and tune hyperparameters, you can implement the following change: in [app.py](app.py#L12), set `production=False` when calling `create_app()`:

```python
app = create_app(production=False)
```


### Dashboard

You can access a live version of the app at: https://ged.nicolepaul.io/. Please note that the live version is hosted on a low cost server and therefore can be slow during certain analysis tasks or if multiple users are making requests at once.

To install the app locally:

1. Clone the repository:
```bash
git clone <repository-url>
cd dash-global-eq-displacement
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python app.py
```

The app will be available at `http://localhost:8050`


In production, you can also run the app as follows:

```bash
gunicorn app:server
```

## Acknowledgments

This research was financially supported by the Internal Displacement Monitoring Centre (IDMC), University College London (UCL), and the Willis Towers Watson (WTW) Research Network. Technical support was also provided by the Global Earthquake Model (GEM) Foundation and United Nations University Institute for Environment and Human Security
(UNU-EHS).

This research was made possible through the contribution of many experts around the world, including engineers, civil servants, and humanitarians. In some cases, these contributors provided housing damage or population displacement data, some of which was used directly and some of which was used to triangulate and verify data from other sources. In other cases, these contributors helped identify reliable national or local sources of data, facilitated connections with relevant contacts in civil protection or national ministries, offered qualitative contextual evidence related to displacement drivers, or assisted with translations between languages and damage scales. We gratefully acknowledge these contributions below.

### Global
Al Mouayed Bellah Nafeh — GEM Foundation

Anirudh Rao — GEM Foundation

Catarina Costa — GEM Foundation

Chris Fairless — UNU-EHS

Justin Ginnetti — IFRC

Lana Todorovic — GEM Foundation

Magdalena Peters — UNU-EHS

Marzia Santini — Joint Research Centre (JRC)

Maxime Souvignet — UNU-EHS

Rob Oakes — UNU-EHS

Sebastien Biasse — University of Geneva

Valerio Salvitti — Joint Research Centre (JRC)

### East Asia and Pacific
Brendon Bradley — University of Canterbury — New Zealand 🇳🇿

Caleb Dunne — Natural Hazards Commission — New Zealand 🇳🇿

Caroline Orchiston — University of Otago — New Zealand 🇳🇿

Chung-Han Chan — National Central University (NCU) — Taiwan 🇹🇼

Finn Scheele — Earth Sciences New Zealand — New Zealand 🇳🇿

Geoffrey Spurr — Natural Hazards Commission — New Zealand 🇳🇿

Jia-Sheng Hung — National Central University (NCU) — Taiwan 🇹🇼

Nick Horspool — Earth Sciences New Zealand — New Zealand 🇳🇿

Rikki Weber — Geoscience Australia — Indonesia 🇮🇩

Sonali Manimaran — Nanyang Technological University — Philippines 🇵🇭

Sukiman Nurdin — Universitas Tadulako — Indonesia 🇮🇩

### Europe and Central Asia
Alen Kadić — Croatian Centre for Earthquake Engineering — Croatia 🇭🇷

Ali Atici — University College London — Türkiye 🇹🇷

Daniela Di Bucci — Dipartimento della Protezione Civile (DPC) — Italy 🇮🇹

Enes Veliu — Albania 🇦🇱

Furkan Narlitepe — IUSS Pavia — Türkiye 🇹🇷

Ioanna Triantafyllou — Hellenic Mediterranean University — Greece 🇬🇷

Josip Atalić — University of Zagreb — Croatia 🇭🇷

Marta Šavor Novak — University of Zagreb — Croatia 🇭🇷

Pouria Kourehpaz — University College London; First Street Foundation — Türkiye 🇹🇷

Tuğrul Sezdirmez — Ministry of Environment Urbanization and Climate Change — Türkiye 🇹🇷

### Latin America and the Caribbean
Alejandro Calderon — GEM Foundation

Diego Nicolas Valdivieso Cascante — Pontificia Universidad Católica de Chile (UC) — Chile 🇨🇱

Jose Gil — Guatemala 🇬🇹

Luis Mixco — Ministerio de Medio Ambiento y Recursos Naturales — El Salvador 🇸🇻

Matias Hube — Pontificia Universidad Católica de Chile (UC) — Chile 🇨🇱

Nicola Tarque — Universidad Politécnica de Madrid — Peru 🇵🇪

Pablo Quinde — Universidad del Azuay — Ecuador 🇪🇨

Rosa Marina Rodríguez Marín — CENAPRED — Mexico 🇲🇽

Salvador Ramos — University of Aveiro — Mexico 🇲🇽

Sandra Cecilia Santa Cruz Hidalgo — Pontificia Universidad Catolica del Peru — Peru 🇵🇪

Sonia Sorto — Dirección General de Protección Civil — El Salvador 🇸🇻

Tamara Cabrera — Chile 🇨🇱

### Middle East and North Africa
Ali Esfandiari — Iran 🇮🇷

Mohamed El Hilali — Morocco 🇲🇦

Mouloud Hamidatou — Research Center in Astronomy, Astrophysics and Geophysics — Algeria 🇩🇿

### South Asia
Natasha Beale — The Asia Foundation — Nepal 🇳🇵

Rashid Rehan — University of Engineering & Technology Peshawar — Pakistan 🇵🇰

### Sub-Saharan Africa
Eleonora Panizza — UniGe; CIMA Foundation — Mozambique 🇲🇿

Innocent Maholi — OpenMap Development Tanzania — Tanzania 🇹🇿
# **US Airfare Analysis: Evaluating Structural Drivers of Ticket Pricing**
### **Description**
Domestic air travel plays a vital role in economic connectivity, enabling business activity, tourism, and personal travel across the United States. For consumers, airfare is one of the most  visible and variable costs of travel, shaped by factors such as distance, demand, airline competition, and market concentration. 
### **Project Summary**
This project investigates the structural drivers of domestic U.S. airfare using market-level data from 2021 to 2025. By moving beyond anecdotal pricing myths, we built a robust predictive model to quantify how market concentration, low-cost carrier (LCC) disruption, and geographical hub dominance interact to determine ticket prices.
### **Business Challenges**
The core challenge was to identify why airline fares vary so significantly across similar routes and how city-level market power influences these prices. Key questions addressed include:
- **Market structure and pricing:** How do fares differ between routes that touch highly  dominant hub cities versus more competitive markets? Do routes with greater low-cost carrier (LCC) penetration exhibit systematically lower fares?
- **Temporal and spatial patterns:** How do average fares evolve across quarters and years?
- **Competition and affordability:** How do dominant-carrier market share and lowest-fare carrier presence relate to average market fares?
- **Modelling and prediction:** Can route-level fares be predicted using distance, demand, competition, and endpoint hub characteristics? Which features contribute most to explaining fare variation across markets?
### **Methodology**
We employed a phased Ordinary Least Squares (OLS) Regression approach to isolate the impact of different forces:
- **Baseline Modelling (Phase 1):** Regressed log-transformed fare against log-distance and log-passengers to account for "economies of scale" in longer flights and high-density routes.
- **Disruption Analysis (Phase 2):** Introduced lcc_volume to test if the physical quantity of budget seats acts as a price ceiling for legacy carriers.
- **Monopoly Power (Phase 3):** Integrated endpoint hub characteristics to measure the premium extracted when a dominant carrier controls airport infrastructure.
- **Full Market Synthesis (Phases 4 & 5):** Finalized a model including "Fixed Effects" (carrier and year dummies) to strip away brand and timing biases.
### **Key Analysis & Results**
The final model reveals three primary drivers of ticket pricing:
- **The Equalizing Force:** LCC Volume is the most consistent check against high prices. It is not just the presence of a budget airline that matters, but also the number of seats it offers. High LCC volume forces even dominant hub carriers to lower fares to remain competitive.
- **The Monopoly Power:** Routes touching highly dominant hubs exhibit a clear price premium. These airlines leverage infrastructure control to maintain higher average fares despite competition.
- **Market Vulnerability:** The model successfully identified "Overpriced Frontiers"—routes where fares are significantly higher than predicted based on distance and volume. These are typically routes with high hub dominance and low LCC penetration.
### **Limitations, Assumptions & Risks**
- **Data Latency:** The DOT data represents historical market averages, not real-time dynamic pricing or "flash sales".
- **Unobserved Factors:** Corporate travel contracts and frequent flyer loyalty bias are not captured, which may keep fares "sticky" on certain business-heavy routes.
- **Regulatory Risk:** Changes in airport slot regulations or FAA policies could disrupt the "Hub Power" our model relies on.
### **Solutions & Recommendations**
- **For Travelers:** Use predicted "Fair Fare" benchmarks to identify if a current ticket price is inflated by hub dominance rather than operational cost.
- **For LCC Strategy:** Target expansion into routes with high "Price Deviations" where tickets are significantly more expensive than the OLS predicted, allowing LCCs to undercut legacy prices while remaining highly profitable.
- **For Policymakers:** Support policies that increase gate access for low-cost carriers at major hubs, as seat volume remains the only effective structural tool for ensuring affordability.

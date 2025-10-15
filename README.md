# Industry-level ESG Pillar Dominance & Greenwashing Detection

This project analyzes ESG (Environmental, Social, and Governance) reports to determine industry and company-level pillar focus and flag potential greenwashing risks using advanced NLP techniques.

### Methodology

- **ESG Text Extraction:** Collects ESG disclosure sections from company reports.
- **Pillar & Greenwashing Vocabulary Expansion:** Augments term lists with industry-specific keywords and WordNet synonyms.
- **TF-IDF Scoring:** Quantifies the importance of E, S, and G pillars for each company and sector.
- **Sentiment Analysis:** Applies VADER and TextBlob to capture tone—but finds that sentiment scores add little value since companies overwhelmingly put a positive spin on reports.
- **Custom Greenwashing Risk Metric:** Developed to overcome sentiment limits, this score incorporates:
  - **Greenwashing Ratio:** Aspirational vs. substantive words
  - **Greenwashing Density:** Aspirational words as a percentage of total
  - **Final Score:** \(0.6 \times \text{Ratio} + 0.4 \times \text{Density}\)
  - **High risk flag:** Ratio ≥ 2.5 and Density > 25

**Excel Output:** Delivers firm-level pillar breakdowns, industry summaries, and greenwashing rankings.

### Features

1. **WordNet-powered term expansion** for robust, customized pillar and greenwashing detection.
2. **TF-IDF quantification** of ESG focus at company and industry level.
3. **Custom greenwashing scoring** that objectively flags reports with excessive aspiration and vagueness.

### Key Results

1. **Sentiment analysis is insufficient:** Nearly all reports are self-promotional; sentiment metrics fail to distinguish real vs. exaggerated claims.
2. **Greenwashing risk reveals true risk:** Scores highlight industries where ESG reporting is especially aspirational or vague amid ongoing controversies.
3. **Pillar scoring exposes industry focus and outliers:**
   - *KLK (Agriculture):* Prioritizes governance, likely to reassure stakeholders and counteract controversy linked to a family-led structure.
   - *ExxonMobil (Oil & Gas):* Emphasizes social responsibility over environmental performance, possibly diverting attention from environmental impact.
   - *Levi’s, Ralph Lauren, M&S (Fashion):* Spotlight sustainability messaging to attract new consumers and differentiate in a crowded market.

### Implementation Notes

A few sample ESG reports are provided within the repository to help you get started. You are encouraged to add more reports or expand the range of industries for your own analysis. This flexibility enables you to adapt the toolkit for broader, comparative, or updated ESG research as needed.

**Note:** The full code process is computationally intensive, as it analyzes nearly 100,000+ words per report, which can be time-consuming. To give you a better idea of the expected output, the PDF file of the complete analysis results has also been uploaded for reference, allowing you to review the detailed insights without waiting for the code to run.

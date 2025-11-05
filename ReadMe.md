# Investigating Emotional Markets

> Predicting market crashes through fine-grained emotional sentiment analysis of retail investor discussions.

---

## Description

This research project explores the relationship between emotional sentiment and financial market behavior, with a particular focus on retail investor activity. As retail investors now constitute approximately one-third of market activity (World Economic Forum), understanding the emotional drivers behind their investment decisions has become increasingly important for predicting market movements.

The project leverages natural language processing (NLP) to analyze emotions expressed in retail investor discussions on Reddit. Using Google's GoEmotions model, we classified text into 27 distinct emotional categories (spanning positive, negative, and ambiguous emotions), with each emotion assigned a probability score from 0 to 1. This fine-grained emotional analysis goes far beyond traditional positive/negative sentiment analysis, enabling us to identify nuanced patterns that precede significant market events.

---

## Methodology

### Data Collection
- Social media posts extracted via Reddit API
- Focus on finance-related subreddits and stock discussions

### Emotion Classification
- Google's GoEmotions model for NLP analysis
- 27 distinct emotional categories classified
- Probability scores (0-1) assigned to each emotion per post
- Categories include: 
  - **Positive:** admiration, amusement, approval, caring, desire, excitement, gratitude, joy, love, optimism, pride, relief
  - **Negative:** anger, annoyance, disappointment, disapproval, disgust, embarrassment, fear, grief, nervousness, remorse, sadness
  - **Ambiguous:** confusion, curiosity, realization, surprise

---

## Research Foundation: Emotions Affect Investment Behavior

Prior research from the Journal of Financial and Quantitative Analysis (JFQA) has established that emotional states directly influence financial decision-making:

- **Excitement** increases investor confidence and willingness to take risks
- **Anxiety** reduces confidence and leads to safer investment choices
- Investors experiencing positive emotions believe outcomes will be favorable and accept more risk
- Investors experiencing negative emotions seek to minimize worry through conservative choices

This established relationship between emotions and investment behavior forms the foundation for using emotional sentiment as a predictive tool for market movements.

---

## Key Finding: Early Detection of the SVB Crisis

**The primary goal of this research was to demonstrate that emotional signals can predict market crises before they occur, giving investors and institutions time to take protective action.**

### Silicon Valley Bank (SVB) Collapse - March 2023

We developed a Fear Index to track banking sector anxiety in the weeks leading up to the Silicon Valley Bank collapse. Our analysis revealed that **emotional fear signals spiked 3-7 days before the actual crash**, providing an early warning window.

![Fear Index - Two Weeks Before SVB Collapse](SVB_Crash.png)*Fear Index tracking from February 23 to March 9, 2023. Note the critical spike on March 8 (marked in orange) - one day before the stock crash (marked in dark red) - exceeding the +2σ threshold.*

#### Timeline of Events:
- **March 8:** Fear index breaches critical +2σ threshold at 0.053 probability
- **March 9:** Stock crash occurs; fear remains elevated at 0.045 probability
- **Early March:** Sustained fear elevation distinguishes this from earlier minor spikes in late February

> **Key Insight:** Investors and banks monitoring this Fear Index could have detected the crisis 3-7 days in advance, allowing time to adjust positions, hedge risk, or withdraw deposits before the collapse.

---

## Distinguishing Market Noise from True Signals

A critical challenge in emotional analysis is **differentiating between temporary sentiment swings and genuine crisis signals**. Our research identified specific patterns that separate routine fluctuations from systemic failures:

### Normal Market Swings:
- Brief, isolated emotional spikes that return to baseline quickly
- Mixed emotional signals without sustained directional movement
- Short-lived fear that doesn't breach critical thresholds

### True Crisis Indicators:
- Sustained elevation of fear-related emotions over multiple days (3-7 day pattern)
- Fear levels exceeding +2σ (two standard deviations) above baseline
- Multiple threshold breaches within a tight window
- Concurrent spikes in nervousness, disgust, and anger

---

## Emotional Correlations with Market Behavior

Our analysis identified which specific emotions correlate with different types of market movements:

![Fear Index - Two Weeks Before SVB Collapse](Emotion_Categories.png)*Left: Emotions correlated with stock direction. Right: Emotions correlated with market volatility.*

### Stock Direction Predictions:

| Emotion | Correlation | Direction |
|---------|-------------|-----------|
| Approval | +0.43 | Upward (strongest) |
| Realization | +0.36 | Upward |
| Embarrassment | +0.26 | Upward |
| Confusion | +0.20 | Upward |
| Caring/Grief/Sadness/Remorse | -0.24 to -0.33 | Downward |

### Volatility Predictions:

| Emotion | Correlation | Effect |
|---------|-------------|--------|
| Fear | +0.45 | Market chaos (strongest) |
| Nervousness | +0.42 | Market chaos |
| Disgust | +0.38 | Market chaos |
| Anger | +0.35 | Market chaos |

### Why These Emotions Matter:

Brief, reactive emotions like fear, anger, and disgust correlate with volatility because they trigger impulsive trading decisions and rapid sentiment shifts. In contrast, sustained emotions like approval indicate longer-term confidence and collective validation, driving directional price movements as more investors build positions over time rather than reacting momentarily.

---

## Future Applications

This emotion-based market analysis framework enables:

1. **Predict Market Crashes** - Detect bank runs, liquidity crises, and systemic failures 3-7 days before collapse by identifying sustained fear patterns exceeding critical thresholds

2. **Separate Noise from Signal** - Distinguish temporary emotional spikes from sustained patterns that indicate genuine directional moves

3. **Identify Emerging Stocks** - Spot securities gaining viral attention before institutional flow follows by tracking approval, excitement, and realization emotions

4. **Track Declining Interest** - Measure when investor enthusiasm fades and capital rotates out by monitoring shifts from positive to negative emotion clusters

---

**Part of this research was conducted for Hack the Burgh's G-Research Challenge**

---

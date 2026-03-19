What is this project about? (Problem Statement)
"If we build solar farms today based on today's weather, will they still be good investments 25 years from now when the climate has changed?"

Currently, companies decide where to build solar farms by looking at:

How much sun shines today

Today's temperature

Land type (farmland, forest, barren)

Distance to power lines

But they almost never ask: "What will the sun and temperature be like in 2050?"
Climate change is already altering cloud cover, temperatures, and weather patterns. A site that is perfect today may become cloudy, too hot, or dusty in a few decades—wasting crores of rupees on underperforming power plants.

This project bridges that gap. We built a statistical framework that combines future climate projections (2050) with a suite of data analysis methods (hypothesis testing, ANOVA, regression, clustering, decision trees) to identify locations where solar PV investments will remain robust even after climate change.

Key Findings (Inference in Simple Words)
After analyzing a realistic synthetic dataset for eastern India, we found:

Finding	What it means
Climate change will significantly reduce suitability	The drop is small on average but can be large in some areas – ignoring it is risky.
Sunlight is king, but heat is the silent killer	Irradiance explains ~90% of suitability, but high temperatures reduce panel efficiency. Best spots have strong sun and cool temperatures.
India has three distinct risk zones	Green zone (high future suitability), yellow zone (moderate), and red zone (low). Planners can use these as a traffic light.
Simple rules work	Decision tree rules: if irradiance > 4.9 kWh/m²/day and temperature < 25°C, suitability is high. Anyone can understand this.
Our models are highly accurate	Linear regression R² = 0.84, logistic regression AUC = 0.95 – you can trust the predictions.
Bottom line: We can now tell energy planners exactly where to build solar farms today so they'll still be profitable in 2050.

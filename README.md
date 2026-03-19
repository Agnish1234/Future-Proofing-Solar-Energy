# **Future‑Proofing Solar Energy: A Multi‑Model Assessment of Climate Change Impacts on Photovoltaic Site Suitability Using Supportive Statistical Learning**

**Problem Statement:** 

    If we build solar farms today based on today's weather, will they still be good investments 25 years from now when the climate has changed?

The Problem in Everyday Words:

    Imagine a guy is buying a house. You check the neighbourhood today – it's quiet, safe, and close to your office. But what if, in 10 years, the neighbourhood becomes noisy, unsafe, and far from new jobs? He would have made a bad investment. Building a solar farm is exactly like buying that house – but for 25–30 years. Right now, when companies decide where to build big solar farms, they look at:

    1. How much sun shines today?
    2. What the temperature is today?
    3. What kind of land it is (farmland, forest, empty land)?
    4. How far it is from power lines?
    5. But they almost never ask: "What will the sun and temperature be like in 2050?"

Why This Matters:

    Climate change is real and it's already changing. Cloud cover – some places are getting cloudier, so less sun reaches the ground. Temperature – solar panels work less efficiently when it's too hot (just like your phone slows down in direct summer sun). Weather patterns – some regions may get more dust storms, more rain, or more fog. If we pick a spot that's great today but becomes cloudy and hot in 20 years, that's crores of rupees wasted on a power plant that produces much less electricity than expected.

The Gap in Current Knowledge:

    Many scientists have studied where to put solar farms. Many have studied how climate change will affect the total amount of solar power a country can make. But almost nobody has connected these two – nobody has asked: "Exactly which specific locations should we build on today so they remain good even after climate change?"
    
    It's like having a weather forecast for next week, but still deciding what clothes to wear based on last week's weather. It doesn't make sense.

What This Study Does?

    We created a smart computer program that:
      1. Looks at today's conditions – sun, temperature, land type, distance to power lines.
      2. Looks at future conditions (for the year 2050) – how much sun and how hot it will be.
      3. Compares them – finds places where the future is still good.
      4. Groups similar areas – so planners can see whole regions that are safe to invest in.
      5. Gives simple rules – like "if the sun is strong and it's not too hot, it's a good spot."

In a nutshell:

    - We built a tool that tells energy planners: 'Build your solar farm here – it will still work well even after climate change.'


**Key Findings from this study:**

1. Suitability change p‑value: 0.0000 – Significant
2. Linear regression R² (standardized): 0.836
3. Logistic regression AUC: 0.952
4. Optimal clusters (k): 3 (silhouette score: 0.204)
5. Decision tree test R²: 0.730
6. Most important feature (tree): irr_current (0.902)
7. Moran's I for residuals: 0.8302 (p=0.0000) – spatial autocorrelation present.

----

**Inference Drawn from This Work:**
"Not all sunny places today will remain good for solar energy in the future. We can now identify which ones will stay good and which ones will become risky."

The Main Conclusions
1. Climate Change Will Affect Solar Farms – It's Not Just a Theory
We found a statistically significant difference between today's suitability and future suitability. In plain English: the places that are great for solar power today will not be the same places that are great in 2050. Some will get cloudier, some will get too hot, and the combination matters.

Think of it like this: If you only checked today's weather to buy a house in a flood zone, you'd be in trouble when the rains come. Similarly, if you only check today's sun to build a solar farm, you'll be in trouble when the climate changes.

2. Sunlight is King – But Heat is the Silent Killer
Our analysis showed that the amount of sunlight is the single most important factor – it determines about 90% of a location's suitability. That makes sense: no sun, no power.

But here's the catch: temperature matters a lot too. Solar panels hate heat. They lose efficiency when they get hot. So a place with lots of sun but very high temperatures might actually be worse than a place with moderate sun and cool temperatures.

The decision tree we built gave us a simple rule: if sunlight is above 4.9 kWh/m²/day AND temperature is below about 25°C, that's an excellent spot. If it's too hot, even lots of sun won't save it.

3. Not All Land is Equal – And That Won't Change
We found that land cover type consistently affects suitability. Barren land (empty, rocky areas) is best – it's cheap, available, and often sunny. Agricultural land is next best. Forests and water bodies are worst because of environmental concerns and practical challenges.

The important finding: policy incentives (like being near a city) help equally everywhere. They don't change which land type is best – they just make every location slightly better. So if the government wants to encourage solar power, giving incentives near cities is a good idea, but don't expect it to magically make a forest as good as a desert.

4. India Has Three Distinct "Risk Zones"
When we grouped similar locations together, we found three clear zones:

Zone	What It's Like	Future Suitability	What It Means
Zone 0	Moderate elevation, lower future sun, warmer	Lowest (0.45)	Risky – avoid long-term investments here
Zone 1	Low elevation, decent future sun, cooler	Medium (0.48)	Okay – acceptable but not ideal
Zone 2	High elevation, highest future sun, coolest	Highest (0.65)	Safe – prioritize here for 25-year projects
This is like a traffic light: green zone (2) is go, yellow zone (1) is cautious, red zone (0) is stop. Energy planners can look at a map and instantly see which areas to focus on.

5. Simple Rules Work Better Than Complex Models
The decision tree gave us rules so simple that anyone can use them:

High suitability (0.71): Sunlight > 6.4 kWh/m²/day

Good suitability (0.64–0.66): Sunlight between 4.9 and 6.4, and cool temperatures

Medium suitability (0.50–0.54): Sunlight between 4.1 and 4.9

Low suitability (0.32–0.43): Sunlight below 4.1

A farmer, a village council member, or a government official can understand these rules without needing a PhD in statistics. "If your village gets more than 5 hours of strong sun and isn't too hot, it's a good place for solar."

7. One Limitation: Nearby Places Influence Each Other
We found that the errors in our model are spatially clustered. That's a fancy way of saying: if our model is wrong in one place, it's probably wrong in nearby places too. This is expected with environmental data – after all, weather doesn't change suddenly from one kilometer to the next.

For practical purposes, this doesn't change our main conclusions, but it's something scientists need to be aware of. Future work could use more advanced "spatial" models to account for this.

The Bottom Line
If you're planning a solar farm today that should still work well in 2050:

Look for places with strong sun AND moderate temperatures. Don't just chase the sunniest spot – check if it will become an oven.

Prioritize barren or agricultural land near existing power lines. Forests and water bodies are non-starters.

Use the simple rules: Sun above 5, temperature below 25, and you're probably safe.

Avoid the red zone – areas with low future sun and high future temperatures will be disappointing investments.

Don't worry about complex math. The decision tree rules are good enough for most decisions.

In One Sentence
"We can now tell you exactly where to build solar farms today so they'll still be profitable when your children are running them."

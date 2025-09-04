# FN-LLM - Agricultural Q&A Large Model by Fengnong AI

[English](readme.md) | [中文](readme_zh.md)

### News

[August 1, 2025] Open-source release of Fengnong AI Large Model (FN-LLM)

[September 4, 2025] Update the open source Fengnong AI model (FN-LLM-V0.2)

### Model Overview
FN-LLM is a core AI product released at the AI FOR AGTECH 2025 conference by Fengnong Holdings. This model integrates massive agricultural knowledge accumulated through years of agricultural services, farming operation solutions, agricultural commodity data from Dafengshou E-commerce platform, and fine-tunes public foundation models through full parameter fine-tuning. It possesses extensive agricultural expertise and precise analytical capabilities, specializing in production problem diagnosis, crop management solutions, and agricultural input usage guidance.

**Key Capabilities**:
- **Professional Agricultural Knowledge**: Deep integration of specialized knowledge from agricultural literature, textbooks, expert knowledge, and service solutions
- **Practical Decision Support**: Provides actionable field management strategies based on comprehensive problem analysis
- **Precise Q&A Capabilities**: Deep analysis of complex agricultural problems with professional, reliable answers
- **Multi-scenario Applications**: Suitable for grower consultations, management decisions, technology promotion, agricultural education, and product marketing

### Data Construction
Training data sources include:
- **Fundamental Agricultural Knowledge**: Wikipedia agricultural entries, classic agricultural literature, textbooks
- **Farming Experience**: Technical solutions and operation logs from years of agricultural services
- **Professional Courses**: Technical training content from "Tiantian Xuenong" platform
- **Agricultural Inputs Database**: Detailed data on pesticides, fertilizers, plant regulators, and tools from Dafengshou Mall

Through professional data distillation and cleaning, we constructed the FN-dataset containing 5000+ high-quality agricultural records.

### Model Architecture
FN-LLM is based on advanced LLM architecture with optimizations:
- Full Parameter Fine-tuning
- Agricultural domain knowledge injection
- Professional terminology understanding and generation optimization
- Enhanced multi-turn dialogue and complex problem handling

### Open-Source Models
- Hugging Face: [https://huggingface.co/fnholding/FN-LLM/tree/main](https://huggingface.co/fnholding/FN-LLM/tree/main)

```
pip install -r requirements.txt 
python infer.py 
```

- GGUF format for Ollama deployment: [https://huggingface.co/fnholding/FN-LLM-GGUF](https://huggingface.co/fnholding/FN-LLM-GGUF)

  ```
   ollama create fn-model -f ./Modelfile
   ollama run fn-model:latest
  ```

  

### Performance Comparison

1. **Question**: What are the specific effects of excessive density on the carbon metabolism of summer maize?
   - **Predicted Answer**: Excessive density causes changes in the carbon-nitrogen metabolism of summer maize plants, reduces the stomatal closure rate, limits CO₂ supply, and decreases the net photosynthetic rate of leaves. At the same time, the carbon allocation to roots decreases, the soil carbon content drops, and the absorption and assimilation of carbon in the above-ground parts are restricted, which directly affects the transfer and accumulation of carbon in grains, ultimately leading to a reduction in dry matter accumulation and insufficient grain filling of maize plants.
   - **Label Answer**: Excessive density leads to a decrease in the activities of Rubisco and PEPC enzymes in the ear-leaves of summer maize, weakens photosynthetic capacity, and affects the synthesis and transportation of soluble sugars and sucrose. Meanwhile, the expression of Zm SPS1 and Gln1-3 genes is down-regulated, the activities of carbon-nitrogen metabolism enzymes decrease, and the contents of sucrose and soluble sugars are significantly reduced. In addition, excessive density may accelerate leaf senescence, reduce chlorophyll content, decrease dry matter accumulation, and thereby weaken carbon metabolism capacity.
2. **Question**: What is the effect of increasing maize planting density on yield?
   - **Predicted Answer**: Appropriately increasing maize planting density can improve yield, but excessive density will lead to poor ventilation and light transmission, more diseases and pests, poor nutrient absorption, and 不协调 (incoordination) between male and female ears, which may instead reduce yield.
   - **Label Answer**: Increasing maize planting density can significantly improve yield when combined with reasonable nutrient management. For example, in 2014, when the planting density of summer maize was increased from 60,000 plants/ha to 75,000 plants/ha, the yield reached 10.7 t/ha. However, yield growth is also comprehensively affected by environmental factors such as meteorological conditions (solar radiation, temperature, rainfall), and it is necessary to optimize the nutrient supply during the key growth periods of crops through nutrient management measures such as split fertilization to achieve maximum yield increase.
3. **Question**: What adverse effects does excessive nitrogen application have on maize leaves?
   - **Predicted Answer**: Excessive nitrogen application causes maize leaves to turn yellow and become smaller in advance, stomata to close, leaves to senesce early, excessive nitrogen content in leaves, and excessive nitrogen application is likely to cause nutrient leaching.
   - **Label Answer**: Excessive nitrogen application leads to excessive nitrogen metabolism in maize leaves, consumes a large amount of photosynthates, reduces the export rate of photosynthates, and causes feedback inhibition of photosynthates on photosynthetic organs. The soluble sugar content in leaves decreases under high nitrogen levels (e.g., nitrogen application rate of 240 kg/hm²), and at the same time, the contribution rate of photosynthetic carbon to grains decreases. Excessive nitrogen also accelerates leaf senescence, accompanied by a decrease in the activities of key photosynthetic enzymes such as Rubisco and PEPCase, leading to a reduction in photosynthetic efficiency.
4. **Question**: What is the best time for weed control at the seedling stage?
   - **Predicted Answer**: Weed control at the seedling stage should be carried out when the crop has 4.5 to 6.5 leaves. It is necessary to choose a period with relatively high temperature, good soil moisture, and weeds having 3 to 4 leaves. In the northwest region, chemical spraying for control is generally carried out from April 15 to May 5 every year.
   - **Label Answer**: The best time for weed control in maize at the seedling stage starts after the maize has 3 leaves, or when the weeds are at the 2-4 leaf stage. Controlling too late will affect the growth of maize.
5. **Question**: How to prevent maize rust?
   - **Predicted Answer**: Prevent maize rust through measures such as reasonable close planting, field management, applying organic fertilizers that combine biological fertilizers and inorganic fertilizers, timely irrigation, strengthening ventilation and moisture removal, removing withered branches, fallen leaves and weeds in the field, and spraying with 75% chlorothalonil wettable powder diluted 500 times after the maize heart leaves silk.
   - **Label Answer**: To prevent maize rust, it is necessary to select disease-resistant varieties, reasonably control the planting density, strengthen the management of water and fertilizer in the field, irrigate in a timely manner, and increase the application of potassium fertilizer.
6. **Question**: How does heavy metal pollution affect the nitrogen supply capacity of soil?
   - **Predicted Answer**: Heavy metal pollution reduces the nitrogen cycle function of soil by destroying the structure and diversity of soil microbial communities, thereby weakening the nitrogen supply capacity of soil. Soil enzyme activities are inhibited by heavy metals, such as the decrease in the activities of dehydrogenase, urease and phosphatase, which are crucial for the decomposition and transformation of organic matter. Soil acidification further accelerates the decomposition rate of organic matter, reduces nutrient accumulation, and at the same time reduces the transformation and release capacity of available nutrients such as nitrate nitrogen and ammonium nitrogen. In addition, heavy metal pollution interferes with the process of plants absorbing nutrients, reduces the utilization of soil nitrogen by plants, and ultimately leads to limited nitrogen transformation in soil.
   - **Label Answer**: Heavy metal pollution leads to a decrease in the nitrogen supply capacity of soil. Cadmium, lead and zinc (except copper) significantly inhibit the mineralization rate of nitrogen, and at the same time inhibit the absorption and transportation of nutrients such as nitrogen by plants, interfere with the metabolic process and material transportation process of plants, and thereby affect the nitrogen supply capacity of soil.
7. **Question**: What are the centrifugation speed and time respectively when extracting total RNA from maize leaves?
   - **Predicted Answer**: The centrifugation speed is 13,000 g, and the time is 10 minutes.
   - **Label Answer**: The centrifugation speed is 13,000 g, and the time is 30 minutes.
8. **Question**: What are the precautions for pH adjustment when preparing the culture medium?
   - **Predicted Answer**: When preparing the culture medium, 1N NaOH or 1N HCl should be used to adjust the pH to 5.7. Since agar and the nutrients in the culture medium will react with acids and alkalis during the preparation process, the pH should be adjusted after the preparation is completed, rather than before cultivation. When adjusting, attention should be paid to the accuracy of the pH, and it should be ensured that the culture medium can still maintain a suitable pH environment after sterilization.
   - **Label Answer**: When preparing the culture medium, the pH needs to be adjusted to 7.0, and 15g of agar powder should be added to the solid culture medium before autoclaving.
9. **Question**: What are the drawbacks of traditional fertilization methods?
   - **Predicted Answer**: Traditional fertilization methods have problems such as unscientific fertilization methods, fertilizer loss and waste caused by not applying according to the season, and low utilization rate. Moreover, the compound fertilizers used have the risk of excessive heavy metals, and long-term use will damage the soil structure and cause excessive heavy metals in crops.
   - **Label Answer**: Traditional fertilization methods result in low nutrient utilization rate, the amount of fertilizer supplied is greater than the crop demand, causing soil acidification, compaction and increased greenhouse gas emissions. Unused nutrients cause non-point source pollution with surface runoff or precipitation infiltration, and are likely to cause soil pollution risks.

### Performance Parameters

```json
{
    "predict_bleu-4": 23.24094375,
    "predict_model_preparation_time": 0.0059,
    "predict_rouge-1": 34.96314375,
    "predict_rouge-2": 12.12781875,
    "predict_rouge-l": 24.933856249999998,
    "predict_runtime": 62.9232,
    "predict_samples_per_second": 0.159,
    "predict_steps_per_second": 0.032
}
```



### Contributors
**FengNong Holdings**  
With technology at its core, FengNong has developed an "Industry-Academia-Intelligence-Products-Investment" ecosystem over the past decade. Our "5+2+N" modern agricultural service model has served over 10 million farmers across 18 provinces, covering 100 million acres of farmland.
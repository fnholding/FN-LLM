# FN-LLM - Agricultural Q&A Large Model by Fengnong AI

[中文](README.md)

### News

[August 1, 2025] Open-source release of Fengnong AI Large Model (FN-LLM)

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

- GGUF format for Ollama deployment: [https://huggingface.co/fnholding/FN-LLM-GGUF](https://huggingface.co/fnholding/FN-LLM-GGUF)

  ```
   ollama create fn-model -f ./Modelfile
   ollama run fn-model:latest
  ```

  

### Performance Comparison
| Question                                                     | Qwen3                                          | FN-LLM                                               |
| ------------------------------------------------------------ | ---------------------------------------------- | ---------------------------------------------------- |
| Fertilization strategy for citrus expansion and ripening stages? | [Detailed technical solution...]               | [Domain-specific optimized solution...]              |
| Damage patterns and control of citrus psyllids?              | [Biological characteristics and prevention...] | [Behavioral analysis and targeted control...]        |
| Optimal basal fertilizer application for citrus?             | [Soil management and application methods...]   | [Nutrient optimization and precision application...] |

*Full comparison table available in Chinese README*

### Contributors
**FengNong Holdings**  
With technology at its core, FengNong has developed an "Industry-Academia-Intelligence-Products-Investment" ecosystem over the past decade. Our "5+2+N" modern agricultural service model has served over 10 million farmers across 18 provinces, covering 100 million acres of farmland.
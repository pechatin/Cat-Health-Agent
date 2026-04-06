# Cat-Health-Agent

Оркестратор для мониторинга и анализа здоровья кота Шипшандера.

```mermaid
graph TD
    Root["cat-health-agent /"]
    SkillMD["SKILL.md<br/>(Оркестратор, Личность, Типографика)"]
    
    subgraph Resources["resources / (База знаний)"]
        Profile["shipshander_profile.md<br/>(Данные о Пациенте)"]
        TableGuide["table_parsing_guide.md<br/>(Расшифровка таблиц)"]
        Refs["reference_ranges.md<br/>(Нормы IRIS/ISFM)"]
        Meds["medication_analysis.md<br/>(Препараты и комплаенс)"]
    end
    
    subgraph SubAgents["sub-agents / (Специфическая логика)"]
        Ther["therapist.md<br/>(Терапевт)"]
        Nutr["nutritionist.md<br/>(Нутрициолог)"]
        Diet["dietitian.md<br/>(Диетолог)"]
        Ophth["ophthalmologist.md<br/>(Окулист)"]
        Dent["dentist.md<br/>(Стоматолог)"]
    end
    
    subgraph Examples["examples / (Примеры)"]
        ExReport["daily_report.md<br/>(Пример анализа)"]
    end

    Root --> SkillMD
    Root --> Resources
    Root --> SubAgents
    Root --> Examples
```

## Структура
- `SKILL.md` — Главные инструкции.
- `sub-agents/` — Узкие специалисты (Терапевт, Нутрициолог, Диетолог, Окулист, Стоматолог).
- `resources/` — База знаний и справочники.
- `examples/` — Примеры обработки.

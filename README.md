# Cat-Health-Agent

**Version: 1.0**
**Update date: 2026-04-06**

Оркестратор для мониторинга и анализа здоровья кота Шипшандера.

```mermaid
graph TD
    Root["cat-health-agent /"]
    SkillMD["SKILL.md<br/>(Оркестратор, Личность, Типографика)"]
    
    subgraph AgentSystem[".agent /"]
        Chlog[".agent/CHANGELOG.md<br/>(История изменений)"]
    end

    subgraph Agents["agents /"]
        subgraph SubAgents["Суб-агенты"]
            Ther["therapist.md<br/>(Терапевт)"]
            Nutr["nutritionist.md<br/>(Нутрициолог)"]
            Diet["dietitian.md<br/>(Диетолог)"]
            Ophth["ophthalmologist.md<br/>(Окулист)"]
            Dent["dentist.md<br/>(Стоматолог)"]
        end
        
        subgraph KnowledgeBase["knowledge-base /"]
            Profile["shipshander_profile.md<br/>(Данные o Пациенте)"]
            TableGuide["table_parsing_guide.md<br/>(Расшифровка таблиц)"]
            Refs["reference_ranges.md<br/>(Нормы IRIS/ISFM)"]
            Meds["medication_analysis.md<br/>(Препараты и комплаенс)"]
        end
    end
    
    subgraph Examples["examples /"]
        ExReport["daily_report.md<br/>(Пример анализа)"]
    end

    Root --> SkillMD
    Root --> AgentSystem
    Root --> Agents
    Root --> Examples
```

## Структура
- `SKILL.md` — Главные инструкции (Оркестратор).
- `.agent/` — Системная папка проекта (CHANGELOG).
- `agents/` — Узкие специалисты (Терапевт, Нутрициолог, Диетолог, Окулист, Стоматолог).
- `agents/knowledge-base/` — База знаний и справочники.
- `examples/` — Приемы и примеры анализа.

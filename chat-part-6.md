## סוכנים ואוטומציה (Skills, MCP, Agents)

**59. כתיבת Skill ראשון (`SKILL.md`)** (🟡)
מה: תיקייה עם YAML frontmatter + הוראות.
למה: היכולת הכי חשובה לשימוש חוזר.
איך: תבנית בסיסית: [פרומפט/תבנית במסמך המלא]
כלים: Claude Code · Claude.ai Skills · [anthropics/skills](https://github.com/anthropics/skills)

**60. Skill למותג + מצגות** (🟡)
מה: Skill שמכיל צבעים, פונטים וכללי שקפים.
למה: כל מצגת נראית «שלנו».
איך: העתיקו דפוס מ־example-skills / document-skills; הוסיפו דוגמאות טובות/רעות.
כלים: Skills · pptx/docx skills

**61. MCP Builder — חיבור כלי פנימי** (🔴)
מה: בונים MCP server שמחבר מערכת פנימית ל־Claude.
למה: Claude עובד על נתונים אמיתיים במקום העלאות.
איך: התחילו מ־mcp-builder ב־anthropics/skills; הגדירו tools קריאה בטוחים קודם.
כלים: Claude Code · MCP · Skills

**62. שילוב Project + Skill + MCP (סוכן מחקר)** (🔴)
מה: לפי הדוגמה של Anthropic: Project לידע, MCP לנתונים, Skill למתודולוגיה.
למה: זה ה«סטאק» המלא לעבודה סוכנית רצינית.
איך: 1. Project «Competitive Intel» + מסמכים.   2. MCP ל־Drive/GitHub/חיפוש.   3. Skill `competitive-analysis`.   4. שאלה אחת שמפעילה הכול.
כלים: Projects · Skills · MCP · (Subagents ב־Code)

**63. Subagent לביקורת קוד בלבד** (🟡)
מה: סוכן עם Read/Grep בלי Write.
למה: ביקורת בלי סיכון לשינוי קבצים.
איך: הגדירו subagent `code-reviewer` עם תיאור ברור מתי להפעיל.
כלים: Claude Code · Subagents

**64. Skill מסוכן עם `disable-model-invocation`** (🟡)
מה: דיפלוי/שליחת הודעות רק בהפעלה ידנית `/deploy`.
למה: מונע פעולות מסוכנות «כי נראה מוכן».
איך: הוסיפו ב־frontmatter: `disable-model-invocation: true`.
כלים: Claude Code Skills

**65. Orchestrator skill (yuv-pilot style)** (🔴)
מה: Skill עליון שמנתב למשימות יצירתיות/פיתוח (בהשראת hoodini/ai-agents-skills).
למה: בפרויקטים גדולים צריך «במאי» שמפצל עבודה.
איך: עייינו ב־[hoodini/ai-agents-skills](https://github.com/hoodini/ai-agents-skills) — skills כמו `yuv-pilot`, `director`.
כלים: Claude Code · Skills

**66. אוטומציית דוחות Excel/PDF** (🟡)
מה: document-skills של Anthropic ל־xlsx/docx/pptx/pdf.
למה: דוחות מעוצבים בלי מאבק ידני.
איך: ב־Claude Code: `/plugin marketplace add anthropics/skills` ואז התקינו `document-skills`.
כלים: Claude Code · Skills

**67. Artifact חי עם MCP** (🔴)
מה: דשבורד שמושך נתונים מ־Calendar/Asana/Slack בכל פתיחה (לפי יכולות עדכניות).
למה: סטטוס תמיד טרי לשיתוף בארגון.
איך: `בנה Artifact דשבורד משימות פתוחות מ־[כלי]. כל צופה יאשר חיבור בעצמו.`
כלים: Artifacts · MCP

**68. רצף סוכנים: Plan → Implement → Review** (🔴)
מה: סוכן תכנון (Explore/Plan), סוכן מימוש, סוכן ביקורת.
למה: פחות זיהום הקשר ופחות באגים.
איך: ב־Claude Code השתמשו ב־fork/subtask לפי התיעוד העדכני; אל תערבבו תכנון ומימוש באותו הקשר ארוך.
כלים: Claude Code · Subagents

**69. Computer use לאוטומציית UI (API)** (🔴)
מה: דרך ה־API — צילומי מסך + קליקים בסביבה מבוקרת.
למה: כשאין API טוב למערכת ישנה.
איך: קראו את [Computer use tool](https://platform.claude.com/docs/en/agents-and-tools/tool-use/computer-use-tool); הריצו רק בסביבת sandbox.
כלים: API · Computer use

**70. בדיקות Webapp עם skill ייעודי** (🔴)
מה: skill לבדיקת אפליקציית ווב (כמו webapp-testing בדוגמאות Anthropic).
למה: רגרסיה מהירה על UI קריטי.
איך: התקינו example-skills ובקשו תרחיש בדיקה מקצה לקצה.
כלים: Claude Code · Skills

**71. סוכן תיעוד שרץ אחרי שינוי קוד** (🟡)
מה: אחרי PR — עדכון README/CHANGELOG אוטומטי בהצעה (לא push לבד).
למה: תיעוד לא נשאר מאחור.
איך: Skill `update-docs` שמופעל ידנית אחרי מיזוג.
כלים: Claude Code · Skills

**72. שרשרת פרומפטים (Prompt chaining) בלי סוכנים** (🟢)
מה: שלב 1 מפיק outline → שלב 2 מרחיב → שלב 3 עורך.
למה: איכות גבוהה יותר מפרומפט אחד ענק.
איך: שמרו את פלט שלב 1 כ־Artifact/קובץ והזינו לשלב 2 במפורש.
כלים: Claude.ai · Artifacts

# Windows: Claude Code + OmniRoute — все нюансы

## 1. Claude Code

```powershell
npm install -g @anthropic-ai/claude-code
```

### Если видишь npm warn install-scripts

```powershell
npm install -g --allow-scripts=@anthropic-ai/claude-code
```

Проверка:
```powershell
claude --version
```

## 2. Ошибка: Имя "git" не распознано

PowerShell не знает git — он не установлен или не в PATH.

### Вариант A — установить Git
1. Скачай: https://git-scm.com/download/win
2. Установи (можно всё по умолчанию)
3. **Закрой и заново открой** PowerShell
4. Проверь: `git --version`

### Вариант B — без Git (ZIP)
1. Открой https://github.com/diegosouzapw/OmniRoute
2. Code → **Download ZIP**
3. Распакуй
4. `cd путь\k\OmniRoute`

## 3. OmniRoute (обход лимитов)

```powershell
git clone https://github.com/diegosouzapw/OmniRoute.git
cd OmniRoute
npm install
npm run dev
```

В **другом** окне PowerShell:
```powershell
omniroute setup-claude
omniroute launch
```

Инструкция: https://github.com/diegosouzapw/OmniRoute/wiki/Claude-Code-Configuration

## 4. DeepSeek Harness (без Claude)

```powershell
npx @deepseek-ai/dsh web
```
→ http://127.0.0.1:3080

## 5. CLAUDE.md

```
# Claude Rules
- Не переусложняй
- Не домысливай
- Не лезь в чужой код без просьбы
- Всегда перепроверяй перед «готово»
```

## Частые ошибки

| Ошибка | Решение |
|--------|--------|
| git не распознан | Установи Git или Download ZIP |
| install-scripts | `npm install -g --allow-scripts=@anthropic-ai/claude-code` |
| claude не найден | Перезапусти PowerShell |
| OmniRoute | `npm run dev` оставь открытым; setup — в другом терминале |

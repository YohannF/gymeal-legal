# D&eacute;ploiement des Documents L&eacute;gaux sur GitHub Pages

## Option 1: Repository D&eacute;di&eacute; (Recommand&eacute;)

### &Eacute;tape 1: Cr&eacute;er le repository

```bash
# Cr&eacute;er un nouveau dossier
mkdir ~/gymeal-legal
cd ~/gymeal-legal

# Copier les fichiers
cp /Users/yohann/Documents/gymeal-Worktree-C/docs/legal/*.md .
cp /Users/yohann/Documents/gymeal-Worktree-C/docs/legal/index.html .

# Initialiser git
git init
git add .
git commit -m "Initial legal documents"

# Cr&eacute;er le repo sur GitHub (via gh CLI ou manuellement)
gh repo create gymeal-legal --public --source=. --push
```

### &Eacute;tape 2: Activer GitHub Pages

1. Aller sur https://github.com/YohannF/gymeal-legal/settings/pages
2. Source: "Deploy from a branch"
3. Branch: `main` / `/ (root)`
4. Cliquer "Save"

### &Eacute;tape 3: URLs finales

Apr&egrave;s d&eacute;ploiement (2-3 minutes), tes URLs seront :

- **Privacy Policy FR**: `https://yohannf.github.io/gymeal-legal/privacy-fr.html`
- **Privacy Policy EN**: `https://yohannf.github.io/gymeal-legal/privacy-en.html`
- **Terms FR**: `https://yohannf.github.io/gymeal-legal/terms-fr.html`
- **Terms EN**: `https://yohannf.github.io/gymeal-legal/terms-en.html`

**Pour App Store Connect**, utilise la version EN :
- Privacy Policy URL: `https://yohannf.github.io/gymeal-legal/privacy-en.html`

---

## Option 2: Utiliser un service tiers

### Notion (Plus simple)
1. Cr&eacute;er une page Notion
2. Coller le contenu markdown
3. "Share to web" &rarr; obtenir l'URL publique

### Google Docs (Alternative)
1. Cr&eacute;er un document Google Docs
2. File &rarr; Share &rarr; "Anyone with the link"
3. Utiliser l'URL de partage

---

## V&eacute;rification App Store

Apple v&eacute;rifie que :
1. L'URL est accessible publiquement
2. Le contenu est pertinent (privacy policy r&eacute;elle)
3. Les informations de contact sont pr&eacute;sentes

**Checklist avant soumission :**
- [ ] URL accessible sans login
- [ ] Contenu en anglais (ou langue de l'app)
- [ ] Email de contact visible
- [ ] Mention des donn&eacute;es collect&eacute;es
- [ ] Mention des services tiers (Firebase, OpenAI)

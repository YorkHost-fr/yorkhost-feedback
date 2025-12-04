# YorkHost Feedback - Labels GitHub

## 🏷️ Labels à créer

Aller dans **Settings > Labels** puis créer ces labels :

---

### 📌 Statut / Status

| Label | Couleur | Description |
|-------|---------|-------------|
| `status: triaged` | `#5319E7` | Reviewed by team / Examiné par l'équipe |
| `status: confirmed` | `#0E8A16` | Bug confirmed / Bug confirmé |
| `status: in-progress` | `#FBCA04` | Currently being worked on / En cours de traitement |
| `status: next-patch` | `#1D76DB` | Scheduled for next update / Prévu pour la prochaine MAJ |
| `status: released` | `#0E8A16` | Fixed/Released / Corrigé/Déployé |
| `status: wontfix` | `#FFFFFF` | Won't be fixed / Ne sera pas corrigé |
| `status: duplicate` | `#CFD3D7` | Already reported / Déjà signalé |
| `status: need-info` | `#D93F0B` | Waiting for more info / En attente d'informations |

---

### 🎯 Type

| Label | Couleur | Description |
|-------|---------|-------------|
| `type: bug` | `#D73A4A` | Something isn't working / Quelque chose ne fonctionne pas |
| `type: feature` | `#A2EEEF` | New feature request / Demande de fonctionnalité |
| `type: improvement` | `#7057FF` | Enhancement to existing feature / Amélioration |
| `type: question` | `#D876E3` | General question / Question générale |

---

### 🎮 Service

| Label | Couleur | Description |
|-------|---------|-------------|
| `service: game-server` | `#B60205` | FiveM, Minecraft, Palworld, Valheim... |
| `service: vps` | `#0052CC` | VPS Hosting |
| `service: web` | `#006B75` | Web Hosting / Hébergement Web |
| `service: panel` | `#5319E7` | Client Panel / Panel Client |
| `service: billing` | `#FBCA04` | Billing/Payments / Facturation |
| `service: network` | `#1D76DB` | Network/Connectivity / Réseau |

---

### ⚡ Priorité / Priority

| Label | Couleur | Description |
|-------|---------|-------------|
| `priority: critical` | `#B60205` | Urgent - Service down / Urgent - Service HS |
| `priority: high` | `#D93F0B` | High priority / Priorité haute |
| `priority: medium` | `#FBCA04` | Medium priority / Priorité moyenne |
| `priority: low` | `#0E8A16` | Low priority / Priorité basse |

---

## 🚀 Script pour créer les labels automatiquement

Tu peux utiliser GitHub CLI (`gh`) pour créer tous les labels d'un coup :

```bash
#!/bin/bash
# Exécuter depuis le repo cloné ou avec gh repo set-default yorkhost-fr/yorkhost-feedback

# Status labels
gh label create "status: triaged" --color "5319E7" --description "Reviewed by team / Examiné par l'équipe"
gh label create "status: confirmed" --color "0E8A16" --description "Bug confirmed / Bug confirmé"
gh label create "status: in-progress" --color "FBCA04" --description "Currently being worked on / En cours de traitement"
gh label create "status: next-patch" --color "1D76DB" --description "Scheduled for next update / Prévu pour la prochaine MAJ"
gh label create "status: released" --color "0E8A16" --description "Fixed/Released / Corrigé/Déployé"
gh label create "status: wontfix" --color "FFFFFF" --description "Won't be fixed / Ne sera pas corrigé"
gh label create "status: duplicate" --color "CFD3D7" --description "Already reported / Déjà signalé"
gh label create "status: need-info" --color "D93F0B" --description "Waiting for more info / En attente d'informations"

# Type labels
gh label create "type: bug" --color "D73A4A" --description "Something isn't working / Quelque chose ne fonctionne pas"
gh label create "type: feature" --color "A2EEEF" --description "New feature request / Demande de fonctionnalité"
gh label create "type: improvement" --color "7057FF" --description "Enhancement to existing feature / Amélioration"
gh label create "type: question" --color "D876E3" --description "General question / Question générale"

# Service labels
gh label create "service: game-server" --color "B60205" --description "FiveM, Minecraft, Palworld, Valheim..."
gh label create "service: vps" --color "0052CC" --description "VPS Hosting"
gh label create "service: web" --color "006B75" --description "Web Hosting / Hébergement Web"
gh label create "service: panel" --color "5319E7" --description "Client Panel / Panel Client"
gh label create "service: billing" --color "FBCA04" --description "Billing/Payments / Facturation"
gh label create "service: network" --color "1D76DB" --description "Network/Connectivity / Réseau"

# Priority labels
gh label create "priority: critical" --color "B60205" --description "Urgent - Service down / Urgent - Service HS"
gh label create "priority: high" --color "D93F0B" --description "High priority / Priorité haute"
gh label create "priority: medium" --color "FBCA04" --description "Medium priority / Priorité moyenne"
gh label create "priority: low" --color "0E8A16" --description "Low priority / Priorité basse"

echo "✅ All labels created!"
```

---

## 💡 Workflow recommandé

1. **Nouvelle issue** → Ajouter `type:` + `service:`
2. **Après review** → Ajouter `status: triaged` + `priority:`
3. **Bug confirmé** → `status: confirmed`
4. **En cours** → `status: in-progress`
5. **Planifié** → `status: next-patch`
6. **Déployé** → `status: released` puis fermer l'issue
7. **Doublon** → `status: duplicate`, lier l'issue originale, fermer

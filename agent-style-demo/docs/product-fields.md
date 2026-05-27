# Canonical Product Fields

This file keeps product language and data fields consistent across apps.

## Shared Fields

| Field | Type | Meaning | Do Not Use |
| --- | --- | --- | --- |
| `account_id` | string | Stable customer account identifier | `acctId`, `customerId` |
| `workspace_id` | string | Stable workspace identifier | `spaceId`, `tenant_id` |
| `owner_email` | string | Account owner's email address | `emailOwner`, `adminEmail` |
| `plan_tier` | enum | Current subscription tier | `plan`, `package` |
| `risk_level` | enum | Operational risk state | `health`, `riskScoreLabel` |
| `monthly_spend` | number | Current month spend in USD | `mrr`, `cost` |
| `last_activity_at` | ISO date | Last meaningful product activity | `lastSeen`, `updatedAt` |

## Risk Levels

Allowed values:

- `low`
- `medium`
- `high`

Display labels:

- `low` -> `Low`
- `medium` -> `Medium`
- `high` -> `High`

## Plan Tiers

Allowed values:

- `starter`
- `growth`
- `enterprise`

Display labels:

- `starter` -> `Starter`
- `growth` -> `Growth`
- `enterprise` -> `Enterprise`

# Quick Summary: Skyscanner's Airflow Repositories

## TL;DR

Skyscanner maintains three distinct Airflow repositories with different purposes:

| Repository | Type | Access | Purpose |
|-----------|------|--------|---------|
| `Skyscanner/airflow` | Apache Airflow Fork | **Public** | Community contributions & standard deployments |
| `Skyscanner/alchemy-airflow-operators` | Custom Library | **Private** | Alchemy platform custom operators |
| `Skyscanner/airflow-skyscanner` | Internal Fork | **Private** | Internal deployments with proprietary features |

## Key Differences

### `Skyscanner/airflow` (Current Repository)
- ✅ **Public repository**
- 🔧 Complete Apache Airflow v2.0.0.dev0
- 🌐 Used for community contributions
- 📊 Standard Airflow functionality

### `Skyscanner/alchemy-airflow-operators`
- 🔒 **Private repository** 
- 🧪 Custom operators library for "Alchemy" data platform
- 📦 Reusable components across multiple Airflow instances
- 🏷️ Tagged: `alchemy`, `weathervane`

### `Skyscanner/airflow-skyscanner`
- 🔒 **Private repository**
- 🏢 Internal fork with Skyscanner-specific modifications
- 🔀 Default branch: `skyscanner-master`
- 🏷️ Tagged: `alchemy`, `fork`, `weathervane`

## When to Use Which?

- **Contributing to Apache Airflow**: Use `Skyscanner/airflow`
- **Developing custom operators**: Use `Skyscanner/alchemy-airflow-operators`
- **Internal deployments**: Use `Skyscanner/airflow-skyscanner`

## Architecture Benefits

1. **🔐 Security**: Private repos for internal code
2. **🔄 Reusability**: Shared operator library
3. **🤝 Community**: Public contributions to upstream
4. **⚡ Efficiency**: Purpose-built for specific needs
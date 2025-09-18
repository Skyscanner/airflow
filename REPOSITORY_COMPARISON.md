# Comparison of Skyscanner's Airflow Repositories

This document provides a comprehensive analysis of the differences between three key Skyscanner Airflow-related repositories.

## Repository Overview

### 1. `Skyscanner/airflow` (Current Repository)
- **Type**: Fork of Apache Airflow
- **Purpose**: Main Skyscanner fork of Apache Airflow (currently at version 2.0.0.dev0)
- **Status**: Public repository
- **Key Characteristics**:
  - Direct fork of the official Apache Airflow project
  - Maintains Apache Airflow branding and structure
  - Contains the full Airflow codebase with potential Skyscanner-specific modifications
  - Latest commit: [AIRFLOW-4862] Fix bug for earlier change to allow using IP as hostname
  - Branches include: master, v1-10-stable, v1-9-stable, v1-8-stable

### 2. `Skyscanner/alchemy-airflow-operators`
- **Type**: Custom Airflow operators library
- **Purpose**: 🧪A library for Alchemy Airflow Operators
- **Status**: Private repository
- **Key Characteristics**:
  - Focused library containing custom Airflow operators for Skyscanner's "Alchemy" platform
  - Tagged with "alchemy" and "weathervane" topics
  - Created: September 2, 2025
  - 3 open issues
  - Appears to be part of Skyscanner's internal data platform ecosystem

### 3. `Skyscanner/airflow-skyscanner`
- **Type**: Fork of official Apache Airflow repository
- **Purpose**: Fork of official Apache Airflow repository (https://github.com/apache/airflow)
- **Status**: Private repository
- **Key Characteristics**:
  - Described as a fork of the official Apache Airflow repository
  - Tagged with "alchemy", "fork", and "weathervane" topics
  - Default branch: "skyscanner-master" (not "master")
  - Created: September 2, 2025
  - 3 open issues
  - More recent creation date suggests it may be a newer, more specialized fork

## Key Differences

### Architecture & Purpose

1. **`Skyscanner/airflow`** (Current):
   - **Full Airflow Distribution**: Complete Apache Airflow installation
   - **Public Facing**: Likely used for community contributions or public deployment
   - **Version**: 2.0.0.dev0 (development version)
   - **Scope**: Comprehensive workflow orchestration platform

2. **`Skyscanner/alchemy-airflow-operators`**:
   - **Specialized Library**: Custom operators specifically for Alchemy platform
   - **Component-Based**: Focused on extending Airflow capabilities
   - **Internal Use**: Private repository for Skyscanner's data platform
   - **Scope**: Custom operators and hooks for specific use cases

3. **`Skyscanner/airflow-skyscanner`**:
   - **Internal Fork**: Private fork with Skyscanner-specific modifications
   - **Branch Strategy**: Uses "skyscanner-master" as default branch
   - **Recent Creation**: Suggests active development or migration effort
   - **Scope**: Full Airflow with internal customizations

### Usage Patterns

#### Current Repository (`Skyscanner/airflow`)
- General-purpose Airflow deployment
- Community contributions to Apache Airflow
- Public-facing Airflow instance
- Standard Apache Airflow functionality

#### Alchemy Airflow Operators
- Custom operators for data processing workflows
- Integration with Skyscanner's "Alchemy" data platform
- Reusable components across multiple Airflow instances
- Part of the broader "Weathervane" ecosystem (based on topics)

#### Airflow Skyscanner
- Internal Airflow deployment with proprietary modifications
- Skyscanner-specific configurations and customizations
- Private deployment with company-specific features
- Potentially staging environment or specialized deployment

### Development Timeline

Based on creation dates and commit history:
- **`Skyscanner/airflow`**: Established repository with mature commit history
- **`Skyscanner/alchemy-airflow-operators`**: Created September 2025 (recent)
- **`Skyscanner/airflow-skyscanner`**: Created September 2025 (recent)

The simultaneous creation of the latter two repositories suggests a recent architectural decision or reorganization.

## Ecosystem Context

### Related Repositories
The search results reveal an extensive Airflow ecosystem at Skyscanner:
- Multiple domain-specific DAG repositories
- Alchemy-related infrastructure components
- Various data processing pipelines
- Integration with "Weathervane" and other internal platforms

### Topics and Tags
- **Alchemy**: Internal data platform
- **Weathervane**: Appears to be an internal platform/project name
- **Fork**: Indicates relationship to upstream projects
- Various domain-specific tags (robins, callisto, etc.)

## Recommendations

### For Different Use Cases:

1. **Public Contributions**: Use `Skyscanner/airflow`
2. **Custom Operator Development**: Use `Skyscanner/alchemy-airflow-operators`
3. **Internal Deployments**: Use `Skyscanner/airflow-skyscanner`

### Architecture Benefits:
- **Separation of Concerns**: Each repository serves a specific purpose
- **Code Reusability**: Custom operators can be shared across deployments
- **Security**: Private repositories for internal modifications
- **Community Engagement**: Public fork for upstream contributions

## Conclusion

The three repositories represent a well-architected approach to managing Airflow at scale:
- **Public fork** for community engagement and standard deployments
- **Custom operators library** for reusable, domain-specific functionality
- **Private fork** for internal deployments with proprietary features

This architecture allows Skyscanner to contribute to the open-source community while maintaining internal capabilities and ensuring proper separation of public and private code.
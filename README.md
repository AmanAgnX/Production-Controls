# Production-Controls
# Aerospace Production Controls & Labor Analysis

*Aerospace & Defense | Program Finance | Production Controls | Labor Analysis*

> Project completed at **Marotta Controls** as a **Cost Finance Intern** within the **Power & Actuation Systems** business unit, supporting **Lockheed Martin’s Precision Strike Missile (PrSM) program for the U.S. Army**.

---

## Overview

The objective was to transform detailed manufacturing and labor information into a structured **production-control and program-finance framework** capable of identifying operational variance and translating it into financially relevant program information.

The analysis connected production routing, standard labor requirements, actual labor performance, efficiency, capacity, cost impact, and forecasting into a recurring production-control process.

---

## Business Problem

Aerospace manufacturing programs operate through sequences of individual production and assembly operations, each consuming labor, time, and production capacity.

Differences between established production standards and actual manufacturing performance can create downstream effects on **cost, schedule, throughput, capacity, and program forecasts**.

The primary challenges were:

* Production activity distributed across multiple operations and stations
* Need to connect operational routing with established labor standards
* Limited visibility into standard versus actual labor consumption
* Difficulty identifying where labor and efficiency variances originated
* Need to identify emerging bottlenecks and capacity constraints
* Need to translate operational deviations into program-finance impacts
* Recurring forecasting and management-review requirements

The problem was therefore both **operational and financial**: production performance needed to be traced from the individual manufacturing operation through its effect on labor, cost, capacity, and the broader program forecast.

---

## What I Built

I developed labor-efficiency and production-control reporting supporting the **PrSM manufacturing environment**.

Key components included:

* Structuring manufacturing activity by product and production operation
* Mapping operational routing and production stations
* Analyzing standard production and labor-hour requirements
* Comparing standard versus actual labor performance
* Building labor-efficiency and variance reports using **Excel, VLOOKUP, and PivotTables**
* Identifying operational and labor variances
* Investigating production bottlenecks with engineering
* Documenting corrective actions
* Supporting capacity and labor-utilization analysis
* Connecting production performance with cost and program forecasting

The framework created a consistent method for moving from detailed manufacturing information to actionable production and financial analysis.

---

# System Architecture

The architecture was structured using a **view-based systems approach**, separating the manufacturing environment, core production-control functions, and analytical implementation.

---

## View 01 — System Context

This view defines the production environment, the information entering the system, and the groups using its outputs.

```text
                 ┌─────────────────────────┐
                 │     MANUFACTURING       │
                 │                         │
                 │ Routing / Labor /       │
                 │ Production Activity     │
                 └────────────┬────────────┘
                              │
                              ▼
                ┌───────────────────────────┐
                │                           │
                │    PRODUCTION CONTROL     │
                │          SYSTEM           │
                │                           │
                └─────────────┬─────────────┘
                              │
             ┌────────────────┼────────────────┐
             ▼                ▼                ▼
        COST FINANCE      ENGINEERING       PROGRAM
                                            MANAGEMENT

        Cost / Forecast   Root Cause /      Program-Level
        Performance      Corrective Action  Review
```

The system creates a common analytical view between **manufacturing execution, engineering investigation, program finance, and management review**.

---

## View 02 — Functional Architecture

This view describes **what the production-control system must do**, independent of the specific analytical tools used.

```text
┌─────────────────────────────┐
│ Define Production Demand    │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Map Operations & Routing    │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Establish Labor Standards   │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Compare Standard vs. Actual │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Analyze Variance &          │
│ Efficiency                  │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Evaluate Capacity &         │
│ Bottlenecks                 │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Evaluate Financial Impact   │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│ Support Program Forecast    │
└─────────────────────────────┘
```

The functional architecture separates the production-control process from the underlying tools and creates traceability from the manufacturing operation to the program forecast.

---

## Stakeholder Alignment

The analysis connected **Cost Finance and Engineering** around a common view of production performance.

Cost Finance evaluated standard and actual labor consumption, efficiency, variance, and financial impact, while engineering supported investigation into operational delays, bottlenecks, and potential corrective actions.

The resulting information supported broader production-control and program-management review within the **Power & Actuation Systems** business unit.

---

## Financial & Decision Logic

Each production operation established an expected amount of labor required to perform the work.

Actual labor consumption could then be compared with that standard:

**Labor Variance = Actual Labor Hours − Standard Labor Hours**

A positive variance indicated that an operation consumed more labor than expected, while a negative variance indicated lower labor consumption relative to the established standard.

Variance could then be traced to individual operations and evaluated for potential effects on efficiency, capacity, cost, and future program requirements.

The decision flow followed:

**Production Demand → Routing → Standard Hours → Actual Hours → Variance → Efficiency / Bottleneck → Cost Impact → Forecast**

This created traceability between the physical manufacturing process and the resulting program-finance implications.

---

## View 03 — Implementation Architecture

This view shows how manufacturing and labor information was transformed into production-control analysis.

```text
                SOURCE DATA
          ┌────────┼────────┐
          ▼        ▼        ▼
       ROUTING   STANDARD   ACTUAL
                 HOURS      LABOR
          │        │        │
          └────────┼────────┘
                   ▼
          DATA STRUCTURING
                   │
                   ▼
       EXCEL / VLOOKUP / PIVOTS
                   │
                   ▼
        STANDARD VS. ACTUAL
                   │
                   ▼
        VARIANCE / EFFICIENCY
                   │
                   ▼
         BOTTLENECK / CAPACITY
              ANALYSIS
                   │
                   ▼
             COST IMPACT
                   │
                   ▼
          PROGRAM FORECAST /
          MANAGEMENT REVIEW
```

Excel, VLOOKUP, and PivotTables were used to structure and analyze production information across operations and compare expected labor requirements with realized performance.

The resulting analytical layer made it possible to identify where production deviations occurred and connect them with program-level cost and forecast considerations.

---

## What the System Measures

| **Management Question**                    | **System View**                                                               |
| ------------------------------------------ | ----------------------------------------------------------------------------- |
| **What should production require?**        | Routing, production time, standard labor hours, and labor requirements        |
| **How is production actually performing?** | Actual labor hours, labor utilization, throughput, and efficiency             |
| **Where are deviations occurring?**        | Labor variance, operational variance, bottlenecks, and capacity constraints   |
| **What is the program impact?**            | Labor cost, capacity requirements, forecast pressure, and program performance |

---

## Business Impact

The framework created a structured connection between **manufacturing execution and program-finance performance**.

It enabled production activity to be evaluated through the chain:

**Production → Labor → Variance → Efficiency / Capacity → Cost → Forecast → Program Performance**

By comparing standard and actual labor performance at the operational level, the analysis improved visibility into where labor inefficiencies and production bottlenecks were developing.

The framework also provided a structured basis for investigating those deviations with engineering, documenting corrective actions, and translating operational performance into financially relevant information for forecasting and management review.

The broader value of the system was its ability to convert detailed manufacturing activity into a **program-level view of cost, capacity, and performance**.


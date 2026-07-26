# Representative DAX measures

The following measures document key logic used in or aligned with the public dashboard.

## Total Applications

```DAX
Total Applications =
DISTINCTCOUNT(PowerBICleanTable[Application ID])
```

## Interview Rate

```DAX
Interview Rate =
DIVIDE(
    [Interview Applications],
    [Total Applications],
    0
)
```

## Data Through Label

```DAX
Data Through Label =
"Data through: "
    & FORMAT(
        MAX(PowerBICleanTable[Date Applied]),
        "MMM d, yyyy"
    )
```

## Public example: Pending Applications Older Than 30 Days

This public example is aligned with the dashboard's documented aging logic.

```DAX
Pending Applications Older Than 30 Days =
CALCULATE(
    [Total Applications],
    PowerBICleanTable[Status] = "Pending",
    PowerBICleanTable[Days Since Applied] > 30
)
```

## Notes

- `Application ID` is used as the distinct application key.
- Aging logic applies only to records currently marked `Pending`.
- The public repository does not include the original record-level model.

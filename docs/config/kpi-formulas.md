# KPI Formula Specifications

## Engagement Rate
ROUND((SUM(Page post engagements) / SUM(Total reach)) * 100, 2)

## Reach Growth (with zero-guard fix - BUG-01)
CASE WHEN SUM(Post organic reach) = 0 THEN 0
     ELSE ROUND(((SUM(Total reach) - SUM(Post organic reach))
          / SUM(Post organic reach)) * 100, 2)
END

## Viral Reach Percentage
ROUND((SUM(Viral reach) / SUM(Total reach)) * 100, 2)

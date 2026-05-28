# Facebook Insights Field Mapping

## Field Alias Normalization (BUG-02 fix)
The Supermetrics connector returns field names with different 
capitalization than API documentation.

Normalized mappings applied at connector configuration:
- "page post engagements" → Page post engagements
- "total reach" → Total reach  
- "post organic reach" → Post organic reach
- "viral reach" → Viral reach
- "post type" → Post type

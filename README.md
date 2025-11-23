MonsterSearch
--------------------
Version: 1.0.0
Author: Yanny Sanmiguel – https://ysanmiguel.com

If you find MonsterSearch useful, consider supporting its continued development.
I have many ideas for new MODX tools and apps — your support helps me keep creating and improving tools for everyone.

https://modxmonster.com/donate

--------------------
Overview
--------------------
MonsterSearch enhances the MODX Manager search with customizable wildcard prefixes,
fuzzy matching, user/resource ID filters, and exact quotes ('...') or ("...").

--------------------
Compatibility
--------------------
- MODX Revolution 2.8.6+ (tested on 2.8.7 / 2.8.8) and 3.x
- PHP 7.4+ (minimum), recommended 8.1+

--------------------
Features
--------------------
- Wildcard prefixes (configurable in System Setting: monstersearch.wildcards)
- Multiple include-type prefixes (e.g. $@ header)
- Type exclusion with -<prefix> (e.g. footer -* -@)
- Exact search with quotes: '23' (ID 23), "footer chunk" (exact name)
- ~ID exact filter (e.g. @~25)
- Fuzzy matching (configurable threshold)
- Users (^) and Resources (#) support

--------------------
Installation
--------------------
1. Install the transport package via Package Manager.
2. Go to System Settings → Namespace: monstersearch.
3. Adjust monstersearch.wildcards, monstersearch.fuzzy_threshold, or monstersearch.debug if needed.
4. Clear cache and reload the Manager.

--------------------
Usage examples
--------------------
$ header          → only Chunks containing "header"
$@ header         → Chunks or Plugins with "header"
footer -*         → with "footer" excluding TVs
@~25              → only Plugin with ID 25
'23'              → only item with ID 23 (exact)
$ "footer chunk"  → only Chunk named exactly "footer chunk"

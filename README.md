# PERFORM-DATA-HANDLING-USING-DATA-FRAMES-CREATION-INSPECTION-SORTING-FILTERING-MERGING-AND-GROUPING-
import pandas as pd
df = pd.DataFrame({
&#39;Name&#39;: [&#39;Alice&#39;, &#39;Bob&#39;, &#39;David&#39;],
&#39;Age&#39;: [25, 32, 47],
&#39;City&#39;: [&#39;NY&#39;, &#39;LA&#39;, &#39;NY&#39;],
&#39;Salary&#39;: [70000, 90000, 120000]
})
print(df)
print(df.head(), df.shape)
print(df.sort_values(&#39;Age&#39;))
print(df[df[&#39;Age&#39;] &gt; 30])
dept = pd.DataFrame({
&#39;Name&#39;: [&#39;Alice&#39;, &#39;Bob&#39;, &#39;David&#39;],
&#39;Dept&#39;: [&#39;HR&#39;, &#39;Eng&#39;, &#39;Eng&#39;]
})
merged = pd.merge(df, dept, on=&#39;Name&#39;)
print(merged)
print(df.groupby(&#39;City&#39;)[&#39;Salary&#39;].mean())****

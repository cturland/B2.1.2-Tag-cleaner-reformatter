<h2>3) Challenge — Tag cleaner &amp; reformatter (split/join, trimming, case normalisation, filtering)</h2>
<p><strong>Goal:</strong> Work with multiple substrings: splitting, trimming, lowercasing, filtering, and re-joining.</p>

<h3>Task</h3>
<ol>
  <li>Ask the user for a comma-separated list of tags (e.g., <code>" Red, blue ,Green, ai, ML , Data-Science "</code>).</li>
  <li>Produce and print:
    <ol type="a">
      <li>A <strong>clean list</strong> of tags: trimmed (no surrounding spaces) and <strong>lowercase</strong>.</li>
      <li>A <strong>kebab string</strong>: the cleaned tags joined with <code>-</code>.</li>
      <li>A <strong>filtered list</strong> that removes any tag with length &lt; 3. Print both the filtered list and its kebab version.</li>
    </ol>
  </li>
</ol>

<h3>Example</h3>
<pre><code>Input:
" Red, blue ,Green, ai, ML , Data-Science "

Clean list:
['red', 'blue', 'green', 'ai', 'ml', 'data-science']

Kebab:
red-blue-green-ai-ml-data-science

Filtered (len &gt;= 3):
['red', 'blue', 'green', 'data-science']

Filtered kebab:
red-blue-green-data-science
</code></pre>

<details>
  <summary><strong>Hints</strong></summary>
  <ul>
    <li><code>parts = raw.split(',')</code></li>
    <li>Trim via <code>.strip()</code></li>
    <li>Lowercase via <code>.lower()</code></li>
    <li>Filter with a list comprehension: <code>[t for t in clean if len(t) &gt;= 3]</code></li>
    <li>Join with <code>"-".join(list_of_tags)</code></li>
  </ul>
</details>

<hr>

<h2>Teacher notes (quick marking cues)</h2>
<ul>
  <li><strong>Exercise 1:</strong> correct use of <code>s[:3]</code>, <code>s[-2:]</code>, <code>s[::-1]</code>; handles short strings gracefully.</li>
  <li><strong>Exercise 2:</strong> correct <code>@</code> split; masking logic respects 1–2 char locals; domain unchanged.</li>
  <li><strong>Exercise 3:</strong> trims spaces, lowercases, filters by length, and uses <code>split</code>/<code>join</code> appropriately.</li>
</ul>

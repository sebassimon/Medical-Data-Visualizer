<h1>Medical Data Visualizer</h1>


<h2>Description</h2>
<p>This project utilizes Python libraries to analyze medical examination data to determine relationships between cardiac disease, body measurements, blood markers, and lifestyle choices.</p>

<h2>Environments & Libraries Used</h2>
<ul>
  <li><b>Python</b></li>
  <li><b>Pandas</b></li>
  <li><b>Matplotlib</b></li>
  <li><b>Seaborn</b></li>
</ul>

<h2>Program Walk-through:</h2>

<h3>Overweight Calculation</h3>
<pre><code>df['overweight'] = (df['weight'] / (df['height'] / 100) ** 2).apply(lambda x: 1 if x > 25 else 0)</code></pre>
<br />

<h3>Data Normalization</h3>
<pre><code>df['cholesterol'] = np.where(df['cholesterol'] == 1, 0, 1)
df['gluc'] = np.where(df['gluc'] == 1, 0, 1)</code></pre>
<br />



<h3>Correlation Heatmap</h3>
<pre><code>sns.heatmap(corr, mask=mask, annot=True, fmt='.1f', cmap='coolwarm', center=0, square=True, linewidths=.5, cbar_kws={"shrink": .5})</code></pre>

<br />
<br />

<h2>Conclusion</h2>
<p>By analyzing the medical data, we can visualize the impact of lifestyle choices on cardiovascular health, assisting in targeted health interventions.</p>

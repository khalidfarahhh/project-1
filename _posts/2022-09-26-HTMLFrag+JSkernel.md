---
keywords: fastai
title: HTML Fragments and Javascript Kernel
toc: true
author: Khalid Farah
categories: [collegeboard]
tags: [python]
nb_path: _notebooks/2022-09026-HTMLFrag+JSkernel.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09026-HTMLFrag+JSkernel.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">function</span> <span class="nx">logIt</span><span class="p">(</span><span class="nx">output</span><span class="p">)</span> <span class="p">{</span>
    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">output</span><span class="p">);</span>
<span class="p">}</span>
<span class="nx">logIt</span><span class="p">(</span><span class="s2">&quot;Hello everyone!&quot;</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Hello everyone!
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="c1">// define a function to hold data for a Person</span>
<span class="kd">function</span> <span class="nx">Person</span><span class="p">(</span><span class="nx">name</span><span class="p">,</span> <span class="nx">nationality</span><span class="p">,</span> <span class="nx">age</span><span class="p">)</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">name</span> <span class="o">=</span> <span class="nx">name</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">nationality</span> <span class="o">=</span> <span class="nx">nationality</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">age</span> <span class="o">=</span> <span class="nx">age</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// define a setter for role in Person data</span>
<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">setRole</span> <span class="o">=</span> <span class="kd">function</span><span class="p">(</span><span class="nx">role</span><span class="p">)</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="nx">role</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// defines the manager</span>
<span class="kd">var</span> <span class="nx">manager</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Fortnite&quot;</span><span class="p">,</span> <span class="s2">&quot;Fortnite&quot;</span><span class="p">,</span> <span class="mf">70</span><span class="p">);</span>
<span class="nx">manager</span><span class="p">.</span><span class="nx">setRole</span><span class="p">(</span><span class="s2">&quot;Manager&quot;</span><span class="p">);</span>

<span class="c1">// JSON conversion from object to a string</span>
<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">toJSON</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
    <span class="kr">const</span> <span class="nx">obj</span> <span class="o">=</span> <span class="p">{</span><span class="nx">name</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">name</span><span class="p">,</span> <span class="nx">nationality</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">nationality</span><span class="p">,</span> <span class="nx">age</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">age</span><span class="p">,</span> <span class="nx">role</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">role</span><span class="p">};</span>
    <span class="kr">const</span> <span class="nx">json</span> <span class="o">=</span> <span class="nx">JSON</span><span class="p">.</span><span class="nx">stringify</span><span class="p">(</span><span class="nx">obj</span><span class="p">);</span>
    <span class="k">return</span> <span class="nx">json</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// player data</span>
<span class="kd">var</span> <span class="nx">players</span> <span class="o">=</span> <span class="p">[</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Ty olsen&quot;</span><span class="p">,</span> <span class="s2">&quot;Mexican&quot;</span><span class="p">,</span> <span class="mf">16</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Khalid Farah&quot;</span><span class="p">,</span> <span class="s2">&quot;Palestinian&quot;</span><span class="p">,</span> <span class="mf">16</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Jeffery Fonseca&quot;</span><span class="p">,</span> <span class="s2">&quot;African-American&quot;</span><span class="p">,</span> <span class="mf">17</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Eli Gilmour&quot;</span><span class="p">,</span> <span class="s2">&quot;Caucasian&quot;</span><span class="p">,</span> <span class="mf">16</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Chris Albertson&quot;</span><span class="p">,</span> <span class="s2">&quot;Syrian&quot;</span><span class="p">,</span> <span class="mf">16</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Ryan McWeeny&quot;</span><span class="p">,</span> <span class="s2">&quot;Caucasian&quot;</span><span class="p">,</span> <span class="mf">16</span><span class="p">),</span>
<span class="p">];</span>

<span class="kd">function</span> <span class="nx">Squad</span><span class="p">(</span><span class="nx">Leader</span><span class="p">,</span> <span class="nx">players</span><span class="p">){</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">manager</span> <span class="o">=</span> <span class="nx">Leader</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">squad</span> <span class="o">=</span> <span class="p">[</span><span class="nx">Leader</span><span class="p">];</span>

    <span class="k">this</span><span class="p">.</span><span class="nx">players</span> <span class="o">=</span> <span class="nx">players</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">players</span><span class="p">.</span><span class="nx">forEach</span><span class="p">(</span><span class="nx">player</span> <span class="p">=&gt;</span> <span class="p">{</span><span class="nx">player</span><span class="p">.</span><span class="nx">setRole</span><span class="p">(</span><span class="s2">&quot;Player&quot;</span><span class="p">);</span> <span class="k">this</span><span class="p">.</span><span class="nx">squad</span><span class="p">.</span><span class="nx">push</span><span class="p">(</span><span class="nx">player</span><span class="p">);</span> <span class="p">});</span>

    <span class="k">this</span><span class="p">.</span><span class="nx">json</span> <span class="o">=</span> <span class="p">[];</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">squad</span><span class="p">.</span><span class="nx">forEach</span><span class="p">(</span><span class="nx">player</span> <span class="p">=&gt;</span> <span class="k">this</span><span class="p">.</span><span class="nx">json</span><span class="p">.</span><span class="nx">push</span><span class="p">(</span><span class="nx">player</span><span class="p">.</span><span class="nx">toJSON</span><span class="p">()));</span>
<span class="p">}</span>

<span class="kd">var</span> <span class="nx">FUT</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Squad</span><span class="p">(</span><span class="nx">manager</span><span class="p">,</span> <span class="nx">players</span><span class="p">);</span>

<span class="nx">Squad</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">_toHtml</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>

    <span class="kd">var</span> <span class="nx">style</span> <span class="o">=</span> <span class="p">(</span>
        <span class="s2">&quot;display:inline-block;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;background:black;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;border: 2px solid grey;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;box-shadow: 0.8em 0.4em 0.4em grey;&quot;</span>
    <span class="p">);</span>

<span class="c1">// HTML Body of Table is build as a series of concatenations (+=)</span>
<span class="kd">var</span> <span class="nx">body</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
<span class="c1">// Heading for Array Columns</span>
<span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
<span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Name&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
<span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Nationality&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
<span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Age&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
<span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Occupation&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
<span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;/tr&gt;&quot;</span><span class="p">;</span>
<span class="c1">// Data of Array, iterate through each row of lakers team</span>
<span class="k">for</span> <span class="p">(</span><span class="kd">var</span> <span class="nx">row</span> <span class="k">of</span> <span class="nx">FUT</span><span class="p">.</span><span class="nx">squad</span><span class="p">)</span> <span class="p">{</span>
  <span class="c1">// tr for each row, a new line</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
  <span class="c1">// td for each column of data</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">name</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">nationality</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">age</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">role</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
  <span class="c1">// tr to end line</span>
  <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
<span class="p">}</span>

 <span class="c1">// Build and HTML fragment of div, table, table body</span>
<span class="k">return</span> <span class="p">(</span>
  <span class="s2">&quot;&lt;div style=&#39;&quot;</span> <span class="o">+</span> <span class="nx">style</span> <span class="o">+</span> <span class="s2">&quot;&#39;&gt;&quot;</span> <span class="o">+</span>
    <span class="s2">&quot;&lt;table&gt;&quot;</span> <span class="o">+</span>
      <span class="nx">body</span> <span class="o">+</span>
    <span class="s2">&quot;&lt;/table&gt;&quot;</span> <span class="o">+</span>
  <span class="s2">&quot;&lt;/div&gt;&quot;</span>
  <span class="p">);</span>

<span class="p">};</span>

<span class="c1">// IJavaScript HTML processor receive parameter of defined HTML fragment</span>
<span class="nx">$$</span><span class="p">.</span><span class="nx">html</span><span class="p">(</span><span class="nx">FUT</span><span class="p">.</span><span class="nx">_toHtml</span><span class="p">());</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">


<div class="output_html rendered_html output_subarea output_execute_result">
<div style='display:inline-block;background:black;border: 2px solid grey;box-shadow: 0.8em 0.4em 0.4em grey;'><table><tr><th><mark>Name</mark></th><th><mark>Nationality</mark></th><th><mark>Age</mark></th><th><mark>Occupation</mark></th></tr><tr><td>Fortnite</td><td>Fortnite</td><td>70</td><td>Manager</td><tr><tr><td>Ty olsen</td><td>Mexican</td><td>16</td><td>Player</td><tr><tr><td>Khalid Farah</td><td>Palestinian</td><td>16</td><td>Player</td><tr><tr><td>Jeffery Fonseca</td><td>African-American</td><td>17</td><td>Player</td><tr><tr><td>Eli Gilmour</td><td>Caucasian</td><td>16</td><td>Player</td><tr><tr><td>Chris Albertson</td><td>Syrian</td><td>16</td><td>Player</td><tr><tr><td>Ryan McWeeny</td><td>Caucasian</td><td>16</td><td>Player</td><tr></table></div>
</div>

</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 


---
title: "Audio Examples"
layout: single
permalink: /audio
author_profile: false
# classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.6"
excerpt: "Experimental results" # "Here you can find the audio files of the different pieces we worked on." - Example of a subtitle
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
---
<html>

</html>


In this page, we introduce a few audio examples drawn from the test set of <a href="https://sigsep.github.io/datasets/musdb.html" target="_blank" rel="noopener noreferrer">MUSDB18</a>. 

---
# Experimental results

## Sample 1

> Source 16kHz
<audio controls>
  <source src="audio/source/11-48.wav"/>
</audio>

<html>
  <table>
    <thread>
      <tr>
        <th>
          <center> Reference </center>
        </th>
        <th>
          <center> Anchor </center>
        </th>
        <th>
          <center> Apollo </center>
        </th>
        <th>
          <center> AudioSR </center>
        </th>
        <th>
          <center> HP-codec+ </center>
        </th>
      </tr>
    </thread>
    <tbody>
      <tr>
        <th>
          <audio controls="">
            <source src="/audio/reference/11-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/reference/11-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/reference/11-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/reference/11-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/reference/11-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>


<br/>

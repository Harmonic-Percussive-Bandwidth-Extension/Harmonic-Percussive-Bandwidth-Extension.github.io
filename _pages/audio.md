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


In this page, we introduce a few audio examples drawn from the test set of <a href="https://sigsep.github.io/datasets/musdb.html" target="_blank" rel="noopener noreferrer">MUSDB18</a>. Each audio example have been downsampled to 16kHz (Anchor) then processed successively by the <a href="https://cslikai.cn/Apollo/" target="_blank" rel="noopener noreferrer">Apollo</a> model, the <a href="https://audioldm.github.io/audiosr/" target="_blank" rel="noopener noreferrer">Apollo</a> model, and our model HP-codec+.

---
# Experimental results

## Example 1

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
            <source src="/audio/anchor/11-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/11-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/11-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/11-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_11.png">
</figure>


## Example 2

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
            <source src="/audio/reference/27-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/27-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/27-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/27-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/27-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_27.png">
</figure>

## Example 3

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
            <source src="/audio/reference/105-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/105-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/105-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/105-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/105-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_105.png">
</figure>

## Example 4

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
            <source src="/audio/reference/131-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/131-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/131-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/131-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/131-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_131.png">
</figure>

## Example 5

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
            <source src="/audio/reference/189-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/189-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/189-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/189-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/189-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_189.png">
</figure>

## Example 6

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
            <source src="/audio/reference/407-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/407-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/407-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/407-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/407-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_407.png">
</figure>

## Example 7

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
            <source src="/audio/reference/535-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/535-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/535-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/535-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/535-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_535.png">
</figure>

## Example 8

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
            <source src="/audio/reference/658-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/658-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/658-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/658-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/658-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_658.png">
</figure>

## Example 9

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
            <source src="/audio/reference/723-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/723-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/723-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/723-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/723-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_723.png">
</figure>

## Example 10

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
            <source src="/audio/reference/792-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/792-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/792-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/792-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/792-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_792.png">
</figure>

## Example 11

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
            <source src="/audio/reference/819-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/819-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/819-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/819-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/819-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_819.png">
</figure>

## Example 12

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
            <source src="/audio/reference/851-48.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/anchor/851-16.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/apollo/851-apo.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/audiosr/851-aud.wav" type="audio/wav">
          </audio>
        </th>
        <th>
          <audio controls="">
            <source src="/audio/hpcodec/851-our.wav" type="audio/wav">
          </audio>
        </th>
      </tr>
    </tbody>
  </table>
</html>
<br/>

<figure>
<img src="/images/spec_comp_sample_851.png">
</figure>

<br/>

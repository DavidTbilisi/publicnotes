---
tags:
  - it/hacking
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/yvNKuZqRmJ4?si=NtArqBMVhsSqMK1k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


```bash
Usage: hashcat [options]... hash|hashfile|hccapxfile [dictionary|mask|directory]...
```


-d Device GPU / CPU digit 
-w Workload profile digit 1-4
-a attack modes digit 
-m type digits
filename
mask


`--attack-mode`
  0 | Straight
  1 | Combination
  3 | Brute-force
  6 | Hybrid Wordlist + Mask
  7 | Hybrid Mask + Wordlist
  9 | Association

`--device types`
  1 | CPU
  2 | GPU
  3 | FPGA, DSP, Co-Processor

`--workload`

| #  | Performance | Runtime | Power Consumption | Desktop Impact  |
|----|-------------|---------|-------------------|-----------------|
| 1  | Low         | 2 ms    | Low               | Minimal         |
| 2  | Default     | 12 ms   | Economic          | Noticeable      |
| 3  | High        | 96 ms   | High              | Unresponsive    |
| 4  | Nightmare   | 480 ms  | Insane            | Headless        |

  

```bash
hashcat -I # show devices
```


```bash
# start with 11 characters and increment till 18
hashcat -i --increment-min 11 --increment-max 18 <mask>
```















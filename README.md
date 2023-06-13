# Artistic-Style Transfer using CNN 
## Main Idea - 

Let’s suppose that we had a way of measuring how different in content two  images are from one another. Which means we have a function that tends to  0 when its two input images (c and x) are very close to each other in  terms of content, and grows as their content deviates. 

We call this function the content loss.

![content-loss function](https://harishnarayanan.org/images/writing/artistic-style-transfer/content-loss.png)
>                          A schematic of the content loss. 

Let’s also suppose that had another function that told us how close in  style two images are to one another. Again, this function grows as its two  input images (s and x) tend to deviate in style. We call this function the  style loss. 

![style-loss function](https://harishnarayanan.org/images/writing/artistic-style-transfer/style-loss.png)

>                          A schematic of the style loss. 

Suppose we had these two functions, then the style transfer problem is  easy to state, right? 
All we need to do is to find an image x that differs  as little as possible in terms of content from the content image c, while  simultaneously differing as little as possible in terms of style from the  style image s. 

Now the crucial bit of insight in this paper by [Gatys et al.](https://arxiv.org/abs/1508.06576) is that the  definitions of these content and style losses are based not on per-pixel  differences between images, but instead in terms of higher level, more  perceptual differences between them. 
Algorithms- I want to investigate how it would work using CNNs. 

## How will this work ?

**Input pictures** – whose style we want to transfer to target picture 
![](https://harishnarayanan.org/images/writing/artistic-style-transfer/edtaonisl.jpg)                
**Target pictures** – pictures that have been made to imbibe the style of the base pictures
![](https://harishnarayanan.org/images/writing/artistic-style-transfer/output_3_0.png)

### Expected Output:
![](https://harishnarayanan.org/images/writing/artistic-style-transfer/c_hugo_bath_s_gothic_cw_0.025_sw_5_tvw_0.5_i_9.png)

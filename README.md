# kcg-ml-screening

# Screening Task

![](RackMultipart20230502-1-zr9oll_html_34b6b55306f35b4b.jpg)

Open **text\_to\_image.py**

- [https://github.com/kk-digital/kcg-ml-](https://github.com/kk-digital/kcg-ml-sd1p4/blob/main/stable_diffusion/scripts/text_to_image.py)[sd1p4/blob/main/stable\_diffusion/scripts/text\_to\_image.py](https://github.com/kk-digital/kcg-ml-sd1p4/blob/main/stable_diffusion/scripts/text_to_image.py)

- Make function that calls the TextEncoder for text prompt and gives embeddingback
  - ^^ Text toembedding

- Make function that takes the encoded embedding, and run the unet/optimizer loop for 20 cycles, returns thelate
  - ^^ Text Embedding is input; optimizer is run; output islatent

- Make a function that takes the latent and runs the auto-encoder, to get outputimage
  - ^^ auto-encoder; input is latent, output isimage

Download Model using bittorrent, using this magnet link:

- magnet:?xt=urn:btih:H6ABMBQRGKWUUR26WM62YVU7HKEEDCLU&dn=v1-5- pruned- emaonly.safetensors&xl=4265146304&tr=udp%3A%2F%2Fexodus.desync.com%3A696 9%2Fannounce

- Kevin also has the torrent file (if you cannot download it, ask forit)
- Time the download time (print time from start to finish, size of file and downloadspeed) For each of those functionsabove
- Show example of generating image from prompt, by calling the three parts of the loopin
series


# 1. Call each function 128times

  1. Each call is called an"inference"
  2. N is sample size, etcN=128
  3. Time total timetaken
  4. Example: output N, output total time, output time perinference
  5. Compare "Batched" vs single call (calling 128 times, vs calling once with 128 input)
  6. Output time taken for batched vs singleinference
  7. Bonus: Only load the part of the model used in the inference instead of thewhole model

Make a function

- to run for ~128prompts
- to time function (single calls vsbatch)

Then compare time of:

- calling function 128 times for batch size1
- time with batch size128

    1. Number of calls/inference (batchsize)
    2. Timetotal
    3. Time perinference


# 1. Linear Interpolation BetweenLatents

1. Use functions above
2. Generate two latents from textinput
3. Interpolate between the latents in. From 0 to 1 in N interviews, etc, N=2, 0.0, 0.5,1.0. To get a ilst of interpolatedlantents
  1. a = 0.0 + n\*(1/num\_divisions)... For n == 0 to n==num\_divisions
4. Run the latents through auto-encoder to getimages
5. Display the images in agrid


# 1.Bonus: SphericalInterpolation

1. Make a notebook like above inkaggle
2. But add section that does spherical interpolation instead oflinear
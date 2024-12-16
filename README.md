# Movie Gen Bench
[Movie Gen](https://ai.meta.com/research/movie-gen/) is a cast of foundation models that generates high-quality, 1080p HD videos with different aspect ratios and synchronized audio.
Here, we introduce our evaluation benchmark "Movie Gen Bench", which includes Movie Gen Video Bench (Section 3.5.2) and Movie Gen Audio Bench (Section 6.3.2), as detailed in the [Movie Gen technical report](https://ai.meta.com/static-resource/movie-gen-research-paper).

To enable fair and easy comparison to Movie Gen for future works on these evaluation benchmarks, we additionally release the non cherry-picked generated videos from Movie Gen on both Movie Gen Video Bench and Movie Gen Audio Bench.

## Table of Contents
- [Movie Gen Video Bench](#movie-gen-video-bench)
- [Movie Gen Audio Bench](#movie-gen-audio-bench)
- [License](#license)
- [Citation](#citation)

## Movie Gen Video Bench
Movie Gen Video Bench consists of 1003 prompts that cover all the different testing aspects/concepts:
 1. human activity (limb and mouth motion, emotions, etc.)
 2. animals
 3. nature and scenery 
 4. physics (fluid dynamics, gravity, acceleration, collisions, explosions, etc.)
 5. unusual subjects and unusual activities. 

Besides a comprehensive coverage of different key testing aspects, the prompts also have a good coverage of high/medium/low motion levels at the same time. 

![Example](images/example.png)

![Prompt Concept Distribution](images/distribution.png)

### Download Video Benchmark

The prompt list ```benchmark/MovieGenVideoBench.txt``` is included in this repo, we additionally release the testing concepts and motion level tags for each prompt in ```benchmark/MovieGenVideoBenchWithTag.csv```. The corresponding generated videos (by Movie Gen) can be [downloaded via this link](https://d1dk99z05ygk7h.cloudfront.net/MovieGenVideoBench.tar.gz?Policy=eyJTdGF0ZW1lbnQiOlt7InVuaXF1ZV9oYXNoIjoid3U2MXBwcWkzN214c2R4ZmRsa3QzcHBuIiwiUmVzb3VyY2UiOiJodHRwczpcL1wvZDFkazk5ejA1eWdrN2guY2xvdWRmcm9udC5uZXRcL01vdmllR2VuVmlkZW9CZW5jaC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3MzQzODA4MTN9fX1dfQ__&Signature=LVdL7x1Skqa3nGMEFIjI09Bq-KgXXxtqUARHQp4qzWjzesZ7k5sbUArzjBp4bt54J6Ywq9OLLcwQUSdUfMmMw2IZw13Oxoi0-Y3JPqtUEszNqfqycA1BV6k4gtKRDlmTkjGqPjn2OEv3YdqqsrZSUPj50y70aqsGhMOvgeD7uYdg3FCUpY26jb7AKWOFDJGZeOm%7EVEKSdqsZdbGdEnNbwYR1-t1j2R0sUmHEPk72TP9lSt2Hpjoy-NihBRK-qah%7EvYXlUEzf2tLKMrqY-1r21Qui6wbGSQmCXJPkwc7y2s4XKf6kskQq1-dntYQDjNIVp-vXWIcFo3dKQ6XTH-Dgyw__&Key-Pair-Id=K15QRJLYKIFSLZ).

Movie Gen Video Bench is also [available on Hugging Face](https://huggingface.co/datasets/meta-ai-for-media-research/movie_gen_video_bench).

## Movie Gen Audio Bench

Movie Gen Audio Bench consists of 527 generated videos and associated sound effects and music prompts
* It covers various ambient environments (e.g., indoor, urban, nature,transportation) and sound effects (e.g., human, animal, objects).
* Movie Gen Video is used to generate videos. We additionally include video prompts used to generate these videos.
* It can be used to evaluate sound effect generation and joint sound effect and background music generation.
* It can be used to evaluate video-to-audio and (text+video)-to-audio generation.

### Download Audio Benchmark 

```benchmark/MovieGenAudioBenchSfx.jsonl``` includes the sound effect prompts used for sound effect generation, and additionally video prompts used for generating testing videos. 
Videos with audio and prompts can be [downloaded via this link](https://d1dk99z05ygk7h.cloudfront.net/MovieGenAudioBenchSfx.tar.gz?Policy=eyJTdGF0ZW1lbnQiOlt7InVuaXF1ZV9oYXNoIjoidDRhdzM0ZmRhanoyNGxvcjE4c3JwbDA0IiwiUmVzb3VyY2UiOiJodHRwczpcL1wvZDFkazk5ejA1eWdrN2guY2xvdWRmcm9udC5uZXRcL01vdmllR2VuQXVkaW9CZW5jaFNmeC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3MzQzODA4MTN9fX1dfQ__&Signature=NNDf3K4H3ySrOaaf3iTbZp0jhnTBoJJ7lT7xnzQVZJtFhrccFSH0V4AJ7ImZE08eE5roNydFIQsmD7QZY-97oJlreRTDIRxx2WwJpXg%7EiO%7E50z6M63ngCE-tj7ju-Qh1T-5708-Adt7QHdMCSaNY60bjX1nOk1NT1VJf2ayZO-ranar-27jjJppOkgDfU17jR6-nFTJpZ6wP3vOPZ5UnYIgj%7Eq2lKDZoaPGhJzHcA5a%7E8xcz-hpiUb0XzGwOQQ1yOJi9%7EZyjutenuiUdxr2iKEpvz9ADzW%7EaI0KOC138d1hDbLy3OPsQht-sF1xkBZQQhPKJrx-Ra9MHQROZUwb6HQ__&Key-Pair-Id=K15QRJLYKIFSLZ).

```benchmark/MovieGenAudioBenchSfxMusic.jsonl``` includes the sound effect and music prompts used for joint sound effect and background music generation, and additionally video prompts used for generating testing videos.
Videos with audio and prompts can be [downloaded via this link](https://d1dk99z05ygk7h.cloudfront.net/MovieGenAudioBenchSfxMusic.tar.gz?Policy=eyJTdGF0ZW1lbnQiOlt7InVuaXF1ZV9oYXNoIjoieGhnNnN3eGdzOGh4dmMyejN4ZjBjZXUwIiwiUmVzb3VyY2UiOiJodHRwczpcL1wvZDFkazk5ejA1eWdrN2guY2xvdWRmcm9udC5uZXRcL01vdmllR2VuQXVkaW9CZW5jaFNmeE11c2ljLnRhci5neiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTczNDM4MDgxM319fV19&Signature=Nh-pFtL0wzwebQLqPfjwl37L-5F8dLG5zq5ZzRL8QzejQ-osdrLM2HzF8hFKJ08k8YTlnkWZMEb9QA4vFSRax4FzBWxnwd13PtSUa1JFhDcqroouNDeH0OFVMdFHEtsvxYTEUayG57bv5qIpCzTlgK2TlpblmrD89UR9ioRblGI7BH4nPH0-Ps1BfMNtxTsdoBEFKnVGxdBmlJf1A4xa6Bv5WYp-ZpJ5NTixyIPw7OaEsdhQSb%7EuQ%7Ekz-ca3XGlRvDqkQF%7EuRb3e-v502q58JziEZE-saHoPcLHqIWWdhtd2OWO8VohRc84Zwfeon5OtnX9940YUZvXt%7Ey-kkPwKeQ__&Key-Pair-Id=K15QRJLYKIFSLZ).


## License

The model is licensed under the [CC-BY-NC license](LICENSE)

## Citation

If you find Movie Gen Bench useful, please consider citing:
```
@misc{polyak2024moviegencastmedia,
      title={Movie Gen: A Cast of Media Foundation Models}, 
      author={Adam Polyak and Amit Zohar and Andrew Brown and Andros Tjandra and Animesh Sinha and Ann Lee and Apoorv Vyas and Bowen Shi and Chih-Yao Ma and Ching-Yao Chuang and David Yan and Dhruv Choudhary and Dingkang Wang and Geet Sethi and Guan Pang and Haoyu Ma and Ishan Misra and Ji Hou and Jialiang Wang and Kiran Jagadeesh and Kunpeng Li and Luxin Zhang and Mannat Singh and Mary Williamson and Matt Le and Matthew Yu and Mitesh Kumar Singh and Peizhao Zhang and Peter Vajda and Quentin Duval and Rohit Girdhar and Roshan Sumbaly and Sai Saketh Rambhatla and Sam Tsai and Samaneh Azadi and Samyak Datta and Sanyuan Chen and Sean Bell and Sharadh Ramaswamy and Shelly Sheynin and Siddharth Bhattacharya and Simran Motwani and Tao Xu and Tianhe Li and Tingbo Hou and Wei-Ning Hsu and Xi Yin and Xiaoliang Dai and Yaniv Taigman and Yaqiao Luo and Yen-Cheng Liu and Yi-Chiao Wu and Yue Zhao and Yuval Kirstain and Zecheng He and Zijian He and Albert Pumarola and Ali Thabet and Artsiom Sanakoyeu and Arun Mallya and Baishan Guo and Boris Araya and Breena Kerr and Carleigh Wood and Ce Liu and Cen Peng and Dimitry Vengertsev and Edgar Schonfeld and Elliot Blanchard and Felix Juefei-Xu and Fraylie Nord and Jeff Liang and John Hoffman and Jonas Kohler and Kaolin Fire and Karthik Sivakumar and Lawrence Chen and Licheng Yu and Luya Gao and Markos Georgopoulos and Rashel Moritz and Sara K. Sampson and Shikai Li and Simone Parmeggiani and Steve Fine and Tara Fowler and Vladan Petrovic and Yuming Du},
      year={2024},
      eprint={2410.13720},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2410.13720}, 
}
```

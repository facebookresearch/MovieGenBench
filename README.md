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

The prompt list ```benchmark/MovieGenVideoBench.txt``` is included in this repo, we additionally release the testing concepts and motion level tags for each prompt in ```benchmark/MovieGenVideoBenchWithTag.csv```. The corresponding generated videos (by Movie Gen) can be [downloaded via this link](https://d14whct5a0wtwm.cloudfront.net/moviegen/MovieGenVideoBench.tar.gz).

Movie Gen Video Bench is also [available on Hugging Face](https://huggingface.co/datasets/meta-ai-for-media-research/movie_gen_video_bench).

## Movie Gen Audio Bench

Movie Gen Audio Bench consists of 527 generated videos and associated sound effects and music prompts
* It covers various ambient environments (e.g., indoor, urban, nature,transportation) and sound effects (e.g., human, animal, objects).
* Movie Gen Video is used to generate videos. We additionally include video prompts used to generate these videos.
* It can be used to evaluate sound effect generation and joint sound effect and background music generation.
* It can be used to evaluate video-to-audio and (text+video)-to-audio generation.

### Download Audio Benchmark 

```benchmark/MovieGenAudioBenchSfx.jsonl``` includes the sound effect prompts used for sound effect generation, and additionally video prompts used for generating testing videos. 
Videos with audio and prompts can be [downloaded via this link](https://d14whct5a0wtwm.cloudfront.net/moviegen/MovieGenAudioBenchSfx.tar.gz).

```benchmark/MovieGenAudioBenchSfxMusic.jsonl``` includes the sound effect and music prompts used for joint sound effect and background music generation, and additionally video prompts used for generating testing videos.
Videos with audio and prompts can be [downloaded via this link](https://d14whct5a0wtwm.cloudfront.net/moviegen/MovieGenAudioBenchSfxMusic.tar.gz).


## License

The model is licensed under the [CC-BY-NC license](LICENSE)

## Citation

If you find Movie Gen Bench useful, please consider citing:
```
@article{polyak2024movie,
  title={Movie Gen: A Cast of Media Foundation Models},
  author={Polyak, Adam and Zohar, Amit and Brown, Andrew and Tjandra, Andros and Sinha, Animesh and Lee, Ann and Vyas, Apoorv and Shi, Bowen and Ma, Chih-Yao and Chuang, Ching-Yao and others},
  journal={arXiv preprint arXiv:2410.13720},
  year={2024}
}
```

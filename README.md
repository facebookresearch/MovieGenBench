# Movie Gen Bench
[Movie Gen](https://ai.meta.com/research/movie-gen/) is a cast of foundation models that generates high-quality, 1080p HD videos with different aspect ratios and synchronized audio.
Here, we introduce our evaluation benchmark "Movie Gen Bench", which includes Movie Gen Video Bench (Section 3.5.2) and Movie Gen Audio Bench (Section 6.3.2), as detailed in the [Movie Gen technical report](https://ai.meta.com/static-resource/movie-gen-research-paper).

To enable fair and easy comparison to Movie Gen for future works on these evaluation benchmarks, we additionally release the non cherry-picked generated videos from Movie Gen on both Movie Gen Video Bench and Movie Gen Audio Bench.

## Table of Contents
- [Movie Gen Video Bench](#movie-gen-video-bench)
- [Movie Gen Audio Bench](#movie-gen-audio-bench)
- [License](#license)

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

The prompt list ```benchmark/MovieGenVideoBench.txt``` is included in this repo, and the corresponding generated videos (by Movie Gen) can be [downloaded via this link](https://d1dk99z05ygk7h.cloudfront.net/MovieGenVideoBench.tar.gz?Policy=eyJTdGF0ZW1lbnQiOlt7InVuaXF1ZV9oYXNoIjoiODRrb3lmNWRqYjRybTd1cTVlcDdvd3dpIiwiUmVzb3VyY2UiOiJodHRwczpcL1wvZDFkazk5ejA1eWdrN2guY2xvdWRmcm9udC5uZXRcLyoiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3MzA4NDU3MzF9fX1dfQ__&Signature=RHY1bOfQ5dsYNuZe2jbnBRUqYyGdOQDZbG2yBywiV4B-lWUfYWH-dxmC8NPfAiDnGUGbdG-IJdvfSENToL8FZHguMKRdKzdN9DcXG7EbZcxz8o6oPInCTTEFOjgdGVWKmzqNowRFjuiNbSOHuBhyAc9CXmftoTR2dNcYS86rzdFAXLggfe1THj87njU7osJk0j6ZsD2ezoAmPZCKH76%7EBnfHQC74Cpo8KqJfHxjKwg5uXBkbV-Q5Ph2e8RTKsNTuRqxjzsQS9sGPjcFMywCzrusVmuBbdJ62DtolFRt9eBExRfZRvXee1xvzWjvlpQYTedfP044ZBieppm43ux-8dw__&Key-Pair-Id=K15QRJLYKIFSLZ).

Movie Gen Video Bench is also [available on Hugging Face](https://huggingface.co/datasets/meta-ai-for-media-research/movie_gen_video_bench).

## Movie Gen Audio Bench

Movie Gen Audio Bench consists of 527 generated videos and associated sound effects and music prompts
* It covers various ambient environments (e.g., indoor, urban, nature,transportation) and sound effects (e.g., human, animal, objects).
* Movie Gen Video is used to generate videos. We additional include video prompts used to generate these videos.
* It can be used to evaluate sound effect generation and joint sound effect and background music generation.
* It can be used to evaluate video-to-audio and (text+video)-to-audio generation.

### Download Audio Benchmark 

```benchmark/MovieGenAudioBenchSfx.jsonl``` includes the sound effect prompts used for sound effect generation, and additionally video prompts used for generating testing videos. 
Videos with audio and prompts can be [downloaded via this link](https://d1dk99z05ygk7h.cloudfront.net/MovieGenAudioBenchSfx.tar.gz?Policy=eyJTdGF0ZW1lbnQiOlt7InVuaXF1ZV9oYXNoIjoiODRrb3lmNWRqYjRybTd1cTVlcDdvd3dpIiwiUmVzb3VyY2UiOiJodHRwczpcL1wvZDFkazk5ejA1eWdrN2guY2xvdWRmcm9udC5uZXRcLyoiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3MzA4NDU3MzF9fX1dfQ__&Signature=RHY1bOfQ5dsYNuZe2jbnBRUqYyGdOQDZbG2yBywiV4B-lWUfYWH-dxmC8NPfAiDnGUGbdG-IJdvfSENToL8FZHguMKRdKzdN9DcXG7EbZcxz8o6oPInCTTEFOjgdGVWKmzqNowRFjuiNbSOHuBhyAc9CXmftoTR2dNcYS86rzdFAXLggfe1THj87njU7osJk0j6ZsD2ezoAmPZCKH76%7EBnfHQC74Cpo8KqJfHxjKwg5uXBkbV-Q5Ph2e8RTKsNTuRqxjzsQS9sGPjcFMywCzrusVmuBbdJ62DtolFRt9eBExRfZRvXee1xvzWjvlpQYTedfP044ZBieppm43ux-8dw__&Key-Pair-Id=K15QRJLYKIFSLZ).

```benchmark/MovieGenAudioBenchSfxMusic.jsonl``` includes the sound effect and music prompts used for joint sound effect and background music generation, and additionally video prompts used for generating testing videos.
Videos with audio and prompts can be [downloaded via this link](https://d1dk99z05ygk7h.cloudfront.net/MovieGenAudioBenchSfxMusic.tar.gz?Policy=eyJTdGF0ZW1lbnQiOlt7InVuaXF1ZV9oYXNoIjoiODRrb3lmNWRqYjRybTd1cTVlcDdvd3dpIiwiUmVzb3VyY2UiOiJodHRwczpcL1wvZDFkazk5ejA1eWdrN2guY2xvdWRmcm9udC5uZXRcLyoiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3MzA4NDU3MzF9fX1dfQ__&Signature=RHY1bOfQ5dsYNuZe2jbnBRUqYyGdOQDZbG2yBywiV4B-lWUfYWH-dxmC8NPfAiDnGUGbdG-IJdvfSENToL8FZHguMKRdKzdN9DcXG7EbZcxz8o6oPInCTTEFOjgdGVWKmzqNowRFjuiNbSOHuBhyAc9CXmftoTR2dNcYS86rzdFAXLggfe1THj87njU7osJk0j6ZsD2ezoAmPZCKH76%7EBnfHQC74Cpo8KqJfHxjKwg5uXBkbV-Q5Ph2e8RTKsNTuRqxjzsQS9sGPjcFMywCzrusVmuBbdJ62DtolFRt9eBExRfZRvXee1xvzWjvlpQYTedfP044ZBieppm43ux-8dw__&Key-Pair-Id=K15QRJLYKIFSLZ).


## License

The model is licensed under the [CC-BY-NC license](LICENSE)

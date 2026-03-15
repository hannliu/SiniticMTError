# SiniticMTError: A Machine Translation Dataset with Error Annotations for Sinitic Languages

This repository provides the dataset introduced in the paper:

- H. Liu, J. Min, E.-S. A. Lee, E. Y. H. Cheung, S.-Y. Hung, E. Chan, S. Qian, R. Liang, K. Hyunh, W. Y. Yip, Y. H. Ng, T. F. Yau, K. I. C. Lo, Y.=W. Wu, R. T.-H. Tsai. [SiniticMTError: A Machine Translation Dataset with Error Annotations for Sinitic Languages](https://arxiv.org/abs/2509.20557v1). Proceedings of Language Resource and Evlauation Conference. Palma, Spain.

We release current Mandarin, Cantonese, Wu Chinese, and Hokkien annotations with 2009, 1402, 68, and 154 annotated sentences, respectively.

## Example
Each datapoint consists of:
* `id`
* `src`: source sentence in English
* `mt`: erroneous machine translation output in target language
* `ref`, a gold-quality reference translation in target language
* `annotations` with span, error type, and error_severity information

```
{
"id": 5,
"src": "28-year-old Vidal had joined Barça three seasons ago, from Sevilla.",
"mt": "28歲嘅維達爾 喺三個賽季之前從塞維利亞加入巴塞爾",
"ref": "28歲嘅維達爾喺三個賽季前由塞爾維亞加盟巴塞。",
"annotations": {
  "annotatedSpans": [
    {"error_text_segment": "從", "start_index": 15, "end_index": 16, "error_type": "Mistranslation", "error_severity": "Minor"},
    {"error_text_segment": "巴塞爾", "start_index": 22, "end_index": 25, "error_type": "Spelling", "error_severity": "Minor"},
    {"error_text_segment": "。", "start_index": 25, "end_index": 26, "error_type": "Typography", "error_severity": "Minor"}
  ]
  }
}
```

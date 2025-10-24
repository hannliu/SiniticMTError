# SiniticMTError Annotation Sample

This repository contains a **preliminary sample** of our **SiniticMTError** dataset, focusing on Mandarin, Cantonese, Wu Chinese, and Hokkien.

## Dataset Info

Each example includes:
- The **source sentence** (`src`)
- The **machine translation output** (`mt`)
- A **reference human translation** (`ref`)
- A list of **annotated error spans** (`annotatedSpans`)
  Each span is labeled with:
  - `error_text_segment`
  - `start_index` and `end_index`
  - `error_type`
  - `error_severity`

Annotations were provided by trained annotators following our proposed guidelines. This sample includes:
- 10 examples in **Mandarin**
- 10 examples in **Cantonese**
- 10 examples in **Wu Chinese**
- 10 examples in **Hokkien**

## Files

- `Mandarin_10_sample.json`: 10 Mandarin examples
- `Cantonese_10_sample.json`: 10 Cantonese examples
- `Wu_10_sample.json`: 10 Wu Chinese examples
- `Hokkien_10_sample.json`: 10 Hokkien examples

## Example Format

``` json
{
  "id": 968,
  "src": "They are listed on the UNESCO World Heritage List.",
  "mt": "他们被列入联合国教科文组织世界遗产名单.",
  "ref": "它们被列入了联合国教科文组织世界遗产名录。",
  "annotatedSpans": [
    {
      "error_text_segment": "他们",
      "start_index": 0,
      "end_index": 2,
      "error_type": "Mistranslation",
      "error_severity": "Minor"
    },
    {
      "error_text_segment": "名单",
      "start_index": 17,
      "end_index": 19,
      "error_type": "Mistranslation",
      "error_severity": "Minor"
    }
  ]
}

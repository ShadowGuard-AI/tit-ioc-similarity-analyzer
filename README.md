# tit-IOC-Similarity-Analyzer
A command-line tool that takes a set of IOCs (domains, IPs, hashes) as input and calculates the similarity score between them using Jaccard index or Levenshtein distance. Jaccard similarity is computed on character 3-gram sets of the normalized IOC, so order and local structure count: unrelated IOCs that share only a suffix score below the default threshold, and reversed strings do not score a perfect match unless they are identical. Identical strings score 1.0. When -o is given and no pair passes the threshold, a header-only CSV is written and a notice states that no pairs passed.

## Install
`git clone https://github.com/ShadowGuard-AI/tit-ioc-similarity-analyzer`

## Usage
`./tit-ioc-similarity-analyzer [params]`

## Parameters
- `-h`: Show help message and exit
- `-i`: A list of IOCs to analyze.
- `-m`: Similarity metric: jaccard or levenshtein
- `-t`: Similarity threshold (0.0 to 1.0)
- `-o`: Output file to save results (CSV format)
- `-v`: Enable verbose logging.

## License
Copyright (c) ShadowStrikeHQ

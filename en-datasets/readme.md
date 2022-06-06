# Source to simulate low-data scenarios

The datasets used to simulate low data scenarios:
*  AG News[^1][^2]: download using the PyTorch datasets

        fom torchtext.datasets import AG_NEWS
        train_iter = AG_NEWS(split='train')
        test_iter = AG_NEWS(split='test')

* SST-2[^3][^4]: files are uploaded here. <code>Val</code> and <code>Train</code> are joined in a set that was used to generate the low-data scenarios.
* TweetEval[^5]: download using HiggingFace datasets

        !pip install datasets
        from datasets import load_dataset
        train = load_dataset('tweet_eval','sentiment','train')
        val = load_dataset('tweet_eval','sentiment','validation')
        test = load_dataset('tweet_eval','sentiment','test')


[^1]: <url>http://groups.di.unipi.it/~gulli/AG_corpus_of_news_articles.html</url>
[^2]: Character-level convolutional networks for text classification.Advances in neural information processing systems. Zhang et al. (2015).
[^3]: Recursive Deep Models for Semantic Compositionality Over a Sentiment Treebank. Socher et al. (2013)
[^4]: https://github.com/YJiangcm/SST-2-sentiment-analysis/tree/master/data
[^5]: SemEval-2017 task 4: Sentiment analysis in Twitter. Rosenthal et al. (2017)

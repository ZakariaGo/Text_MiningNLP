# Text_MiningNLP

The goal of this project is to evaluate different metrics when applying text embeddings ( word2vec and FastText ) to various text collections

{
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "print(\"%.3f\" % adjusted_rand_score(labels, y_kmeans), \"%.3f\" % accuracy_score(labels, y_kmeans), \"%.3f\" % normalized_mutual_info_score(labels, y_kmeans))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Conclusion\n",
    "### En utilisant Word2Vec\n",
    "\n",
    "Methode (ARI, Clustering Accuracy et NMI)/Dataset | Classic | NG5 | NG20 | R8  \n",
    "--- | --- | --- | --- | ---  \n",
    "document représenté par u 1 sans utiliser tf-idf | (0.731, 0.234, 0.659)| (0.120, 0.229, 0.252) | (0.103, 0.048, 0.235) |  0.397 0.010 0.538 \n",
    "document représenté par u 1 en utilisant tf-idf | (0.922, 0.264, 0.877) | (0.450, 0.193, 0.463) | (0.175, 0.033, 0.305) |   0.369 0.014 0.496\n",
    "document représenté par u 1 + u 2 sans utiliser tf-idf | (0.672, 0.268, 0.617) | (0.144, 0.148, 0.199) | (0.062, 0.060, 0.163) |  (0.200, 0.071, 0.305)\n",
    "document représenté par u 1 + u 2 en utilisant tf-idf | (0.705, 0.0576, 0.630) | (0.320, 0.219, 0.330) | (0.146, 0.0597, 0.264) |  0.188 0.051 0.331"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### En utilisant fastText\n",
    "\n",
    "Methode (ARI, Clustering Accuracy et NMI)/Dataset | Classic | NG5 | NG20 | R8  \n",
    "--- | --- | --- | --- | ---  \n",
    "document représenté par u 1 sans utiliser tf-idf | 0.923 0.364 0.884 | 0.039 0.199 0.069 | 0.023 0.049 0.077 | 0.358 0.137 0.469\n",
    "document représenté par u 1 en utilisant tf-idf  | 0.871 0.955 0.813| 0.187 0.215 0.240 | 0.107 0.049 0.217 | 0.345 0.130 0.453\n",
    "document représenté par u 1 + u 2 sans utiliser tf-idf  | 0.766 0.037 0.710 | 0.029 0.198 0.034 | 0.015 0.041 0.055 | 0.210 0.112 0.324\n",
    "document représenté par u 1 + u 2 en utilisant tf-idf | 0.745 0.907 0.667 | 0.183 0.095 0.239 | 0.085 0.085 0.182 | 0.237 0.271 0.342"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. [Classic 3](#Classic_3)\n",
    "- [NG5](#NG5)\n",
    "- [NG20](#NG20)\n",
    "- [Reuters8](#Reuteurs_8)\n",
    "    \n"
   ]
  }
 

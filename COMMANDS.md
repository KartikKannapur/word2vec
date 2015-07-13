
#####Clone Repo
1. git clone https://github.com/KartikKannapur/word2vec.git
2. Run $ make

#####Compile

3. gcc word2vec.c -o word2vec -lm -pthread -O3 -march=native -Wall -funroll-loops -Wno-unused-result
4. gcc word2phrase.c -o word2phrase -lm -pthread -O3 -march=native -Wall -funroll-loops -Wno-unused-result
5. gcc distance.c -o distance -lm -pthread -O3 -march=native -Wall -funroll-loops -Wno-unused-result

#####Download & Unzip
6. http://mattmahoney.net/dc/text8.zip 

#####Run
7. ./word2vec -train text8 -output vectors.bin -cbow 0 -size 200 -window 5 -negative 0 -hs 1 -sample 1e-3 -threads 12 -binary 1
8.  ./distance vectors.bin

> nllb

nllb propose déjà le "Nigerian Fulfulde" et peut être enrichi avec le pular/fula avec le dataset pour français-> peul futa djalon (== pular chez cawoylel)
- https://github.com/refacto-org/MaLiNaLi_fulani/tree/main/fr_ff_2/data

Voici un article détaillé sur comment ajouter une langue sur ce modèle puis l'exposer : 
https://cointegrated.medium.com/how-to-fine-tune-a-nllb-200-model-for-translating-a-new-language-a37fc706b865
L'arti 

If the Colab instance has shut down, you can always load it back from the Google drive where you have saved it

from transformers import NllbTokenizer, AutoModelForSeq2SeqLM
model_load_name = '/gd/MyDrive/models/nllb-fra-fuf-v1'
model = AutoModelForSeq2SeqLM.from_pretrained(model_load_name).cuda()
tokenizer = NllbTokenizer.from_pretrained(model_load_name)
fix_tokenizer(tokenizer)
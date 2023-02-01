Hi,

<img width="740" alt="image" src="https://user-images.githubusercontent.com/9829375/216008654-b42d5695-782e-43e1-bdeb-014f7011dcba.png">

I heard some conversations recently about the potential of this tool – in Arabic – while visiting Amman, Jordan, and so I reached into the online toolkit and was pleased to find that ChataGPT actually handles Arabic quite gracefully.

For some context, Arabic is an RTL (Right-to-left) language with complex morphology that has created all sorts of challenges in translation (e.g. Google Translate continues to perform at a relatively unreliable level for most complex queries and anything beyond a very simple transform). 

The GPT was able to e.g. generate a story in Arabic from an English prompt, translate that story to English. That's cool! 

I was pleased to see that the ChatGPT interface offered by OpenAI also gracefully handled RTL text (though it does not format the whole div correctly). RTL has continued to somehow confound many text editors and formatting interfaces, despite its being implemented successfully over a decade ago. E.g. SublimeText still fails to handle RTL with any grace at all. 

Arabic translation offered by ChatGPT – does it out-perform Google Translate ? [ChatGPT Jan 30 Version. Free Research Preview.]()

<img width="890" alt="image" src="https://user-images.githubusercontent.com/9829375/216008780-c9bbeb3b-bd14-4839-a061-c39d84c2b0d5.png">

<img width="882" alt="image" src="https://user-images.githubusercontent.com/9829375/216008861-2222e840-c33e-4663-9af0-6745f0c30f0d.png">

<img width="864" alt="image" src="https://user-images.githubusercontent.com/9829375/216008961-65781536-7ede-457e-8819-aea73de1b7c3.png">

In the example below, for example, the text-block should be right-aligned, which will lead to the sentence-ending period marks being placed on the left, and the beginning of the sentence being fully aligned on the right.

<img width="888" alt="image" src="https://user-images.githubusercontent.com/9829375/216009680-17def80d-1ba6-4fd7-9813-5dc145df2a41.png">

Compare this with StableDiffusion, which can generate styles without issue, but currently fails to perform linguistic-translation tasks : 
![image](https://user-images.githubusercontent.com/9829375/216010305-4fb5f8fd-7098-47b5-b521-626daf4dd3f1.png)

E.g. "The word 'love' in Arabic calligraphy"
![image](https://user-images.githubusercontent.com/9829375/216010537-3f3f6c94-67cf-4c6a-9d30-ddf37aba5a62.png)

Notably, this one retains the four-character shapes I would expect for translating محبه (م ح ب ه) , though they are "rendered in a more historical style" ;)  aka potentially closer to (l o v e) than their Arabic counterpart.

vs
(same input)
![image](https://user-images.githubusercontent.com/9829375/216010699-06e046d4-edaf-4a67-b92e-2b20a940ba47.png)


I compare "The word 'love' in Sogdian calligraphy"
![image](https://user-images.githubusercontent.com/9829375/216011196-8a671dce-348a-423a-ac20-539d57b89553.png)

& "The word 'love' in Chinese calligraphy"
![image](https://user-images.githubusercontent.com/9829375/216012143-35bf2c41-aca1-48ec-a4c4-b6da5ba57984.png)


"The word 'Love' in calligraphy" suggests that the StableDiffusion conception-space of calligraphy is dominated by Arabic and Chinese examples, which [makes sense](https://en.wikipedia.org/wiki/Calligraphy).



Some context:
I used the ChatGPT interface offered by OpenAI at <https://chat.openai.com/>.

I used the StableDiffusion interface offered by <https://StableDiffusionWeb.com>. 
Note that the following website has no identifying information that I could use to establish organizational legitimacy, (domain is registered in Iceland).

Also, things like this seem to exist now : https://www.reddit.com/r/StableDiffusion/comments/10n3cqo/major_update_automatic1111_photoshop_stable/ 
Have fun and good luck!

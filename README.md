# infinitescrl
*Implementação básica de um Lazy-loader de images utilizando Intersection Observer*
<br>

[Demo ](https://tfnix.github.io/infinitescrl/)


```js
         <div style={singleColumnLayout}>
             {items.map((item, index) => {
                  const isLastItem = items.length === index + 1;
                    return (
                         <div
                             ref={isLastItem ? lastItemRef : null}
                             
.....

```
*É a ultima image? Adicione a referência(lasItemRef) e,  quando a ref. estiver visível, chame a callback - nesse caso o hook useEffect()*

```js
  useEffect(() => {
        setLoading(true);

        setTimeout(() => {
            const newItems = Array.from({ length: 10 }, (_, i) => {
                const itemId = (page - 1) * 10 + i + 1;
                return {
                    id: itemId,
                    title: `Image ${itemId}`,
                    imageUrl: `https://picsum.photos/seed/${itemId * 7}/800/600`
                };
            });
```




<br>
Referência: <br>
https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API

<br> <br>
<b>
PS: made with AI assistence 😎 
</b>

## My Personalized Custom Hooks that i am using for React and Gutenberg Wordpress Editor.

### Purpose for using this
- No need to understand Comeplex redux for the small piece of the task.
- easily share the component data with diffrent components
- Work Like same as useState

## Package Link
- https://www.npmjs.com/package/@vanpariyar/hooks

### use 
```javascript
import { useLocalStorage, useSessionStorage } from '@vanpariyar/hooks'
import { useEffect } from 'react'


const functionalComponent = () => {
    const[ newsArticles, setNewsArticles ] = useSessionStorage( 'newsArticles', InitialValue );

    // OR

    const[ newsArticles, setNewsArticles ] = useLocalStorage( 'newsArticles', InitialValue );

    useEffect(()=>{
        if( newsArticles ) { return };
        setArticles( [ 1, 2, 3 ] )
    },[])
    
}

export default functionalComponent;
```

than in any compnent

```javascript
import { useLocalStorage, useSessionStorage } from '@vanpariyar/hooks'

const otherFunctionalComponent = () => {
    const[ newsArticles, setNewsArticles ] = useSessionStorage( 'newsArticles', InitialValue );

    // OR

    const[ newsArticles, setNewsArticles ] = useLocalStorage( 'newsArticles', InitialValue );

    console.log( newsArticles );
}

export default otherFunctionalComponent;
```
## Credits 
webdev simplified: The `useLocalStorage` hook is inspired by them Thank you.
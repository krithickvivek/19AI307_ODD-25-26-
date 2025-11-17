# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.
## AIM:
To save and restore article content versions using the Memento design pattern.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read article updates one by one, set content, and save each as a memento.
4. Store every saved memento in history so versions can be restored later.
5. Read the index the user wants to restore and fetch that version.
6. If valid, restore the article content; otherwise print “Invalid version”.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Krithick Vivekananda
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}

```

## OUTPUT:
| Input | Expected | Got | Status |
|-------|----------|------|--------|
| 3<br>Initial draft<br>Revised content<br>Final article version<br>2 | Final article version | Final article version | ✓ |
| 4<br>V1<br>V2<br>V3<br>V4<br>5 | Invalid version | Invalid version | ✓ |
| 2<br>Start here<br>Second update<br>0 | Start here | Start here | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program stores each article revision as a memento and restores the correct version when requested.

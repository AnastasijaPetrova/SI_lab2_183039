<h1>Втора лабораториска вежба по Софтверско инженерство </h1>

<h2>Анастасија Петрова, бр. на индекс 183039</h2>
<h3>Група на код:</h3>

Ја добив групата на код 5

<h3>Control Flow Graph</h3>

![GitHub Logo](/Graph.png)

    public List<String> function(List<String> list) {//1
        if (list.size() <= 0) {//2
            throw new IllegalArgumentException("List length should be greater than 0");//3
        }
        List<String> numMines = new ArrayList<>();//4
        for (int i = 0; i < list.size(); i++) {//5.1->int i=0; 5.2->while(i < list.size()); 5.3->i++;
            if (!list.get(i).equals("#")) {//6
                int num = 0;//7
                if (i - 1 >= 0 && list.get(i - 1).equals("#")) {//8
                    num++;//9
                }
                if (i + 1 < list.size() && list.get(i + 1).equals("#")) {//10
                    num++;//11
                }
                numMines.add(String.valueOf(num));//12
            }
	else {//13
                numMines.add(list.get(i));//14
            }
        }//15
        return numMines;//16 
    }//17
    
<h3>Цикломатска комплексност</h3>

Бројот на предикатни јазли = 5 тоа се 2; 5.2; 6; 8; 10.<br>
Бројот на региони = 6.<br>
Цикломатската комплексност на овој код е 6, истата ја добив преку формулата P+1, каде што P е бројот на предикатни јазли. Во случајoв P=5, па цикломатската комплексност изнесува 6.

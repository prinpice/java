# Student

```
import javax.swing.plaf.synth.SynthSeparatorUI;

public class Student {
	String name;
	int korean;
	int math;
	int english;
	int sum;
	double ave;
	String PF;
	
	void showInfo() {
		System.out.println("이름 : " + name);
		//System.out.println("국어점수 : "+ korean);
		//System.out.println("수학점수 : "+ math);
		//System.out.println("영어점수 : "+ english);
		//sum = korean + math + english;
		//ave = sum/ 3.0;
		System.out.println("평균점수 : "+ave+"점");
		//System.out.println("합격여부 : "+((ave >= 60)? "합격" : "불합격"));
		System.out.println("합격여부 : "+PF);
	
	}
}

```


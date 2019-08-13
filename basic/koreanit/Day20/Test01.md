# Test01

```java
// getter, setter는 통상적으로 public로 만듬
// setter는 저장하는 용도(보통 자료형 void)
// jsp에서 getter, setter 안만들면 에러 발생
class Pokemon{
	private String name;
	private int level;
	private boolean alive;
	// 우클릭 -> source -> generate getters and setters
	//   -> select all -> finish
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getLevel() {
		return level;
	}
	public void setLevel(int level) {  // 캡슐화
		if (level >= 1 && level <= 1000) {
			this.level = level;
		}else {
			this.level = 1;
		}
	}
	public boolean isAlive() {
		return alive;
	}
	public void setAlive(boolean alive) {
		this.alive = alive;
	}
}
public class Test01 {
	public static void main(String[] args) {
		Pokemon p1 = new Pokemon();
		// p1.name = "피카츄";
		p1.setName("피카츄");
		
		//p1.level = -10;
		p1.setLevel(-10);
		
		// System.out.println(p1.name);
		System.out.println(p1.getName());
		System.out.println(p1.getLevel());
	}
}

```


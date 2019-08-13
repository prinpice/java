# Quiz02

```java
/*
 * 원본클래스 : Book
 *  필드 : 책이름, 출판사
 *  메소드 : printBook()
 *        => 책이름, 출판사 sysout
 * 자식클래스 : 
 *  1. Novel
 *      필드 : 장르, 작가
 *      메소드 : PrintNovel()
 *            => 책이름, 출판사, 장르, 작가 모두 sysout
 *  2. Textbook
 *      필드 : 과목
 *      메소드 : PrintTextbook()
 *  3. Comic
 *      필드 : 주인공, 가격
 *      메소드 : PrintComic()
 *  => 추가문제 : 자식클래스의 생성자도 만들어보세요.
 */
class Book{
	// 필드
	private String bookName;
	private String publishingCompany;
	
	// 생성자
	public Book(){}
	/*
	 * 자료형이 같아서 둘 중에 하나만 사용이 가능하다.
	public Book(String bookName){
		setbookName(bookName);
	}
	public Book(String publishingCompany){
		setpublishingCompany(publishingCompany);
	}
	*/
	public Book(String bookName, String publishingCompany){
		setbookName(bookName);
		setpublishingCompany(publishingCompany);
	}
	
	// getter
	public String getbookName() {return bookName;}
	public String getpublishingCompany() {return publishingCompany;}
	
	// setter
	public void setbookName(String bookName) {
		this.bookName = bookName;
	}
	public void setpublishingCompany(String publishingCompany) {
		this.publishingCompany = publishingCompany;
	}
	
	// Method
	void printBook() {
		System.out.println("책이름 : " + bookName);
		System.out.println("출판사 : " + publishingCompany);
	}
}
class Novel extends Book{
	// 필드
	private String genre;
	private String writer;
	
	// 생성자
	public Novel(){}
	public Novel(String genre, String writer){
		setgenre(genre);
		setwriter(writer);
	}
	
	// getter
	public String getgenre() {return genre;}
	public String getwriter() {return writer;}
	
	// setter
	public void setgenre(String genre) {
		this.genre = genre;
	}
	public void setwriter(String writer) {
		this.writer = writer;
	}
	
	// Method
	void PrintNovel() {
		printBook();
		System.out.println("장르 : " + genre);
		System.out.println("작가 : " + writer);
	}
	
}
class Textbook extends Book{
	// 필드
	private String subject;
	
	// 생성자
	public Textbook() {}
	public Textbook(String subject) {
		setsubject(subject);
	}
	
	// getter
	public String getsubject() {return subject;}
	
	// setter
	public void setsubject(String subject) {
		this.subject = subject;
	}
	
	// Method
	void PrintTextbook() {
		printBook();
		System.out.println("과목 : " + subject);
	}
}
class Comic extends Book{
	// 필드
	String mainCharacter;
	int price;
	
	// 생성자
	public Comic() {}
	public Comic(String mainCharacter, int price) {
		setmainCharacter(mainCharacter);
		setprice(price);
	}
	
	// getter
	public String getmainCharacter() {return mainCharacter;}
	public int price() {return price;}
	
	// setter
	public void setmainCharacter(String mainCharacter) {
		this.mainCharacter = mainCharacter;
	}
	public void setprice(int price) {
		this.price = price;
	}
	
	// Method
	void PrintComic() {
		printBook();
		System.out.println("주인공 : " + mainCharacter);
		System.out.println("가격 : " + price);
	}
}
public class Quiz02 {
	public static void main(String[] args) {
		Novel n = new Novel();
		
		n.setbookName("JAVA");
		n.setpublishingCompany("A");
		n.setgenre("컴퓨터");
		n.setwriter("jason");
		
		n.PrintNovel();
		
	}
}

```


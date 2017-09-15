# Student_Information_Management_Program

Consol Base의 학생정보 관리 Program 입니다.

----------------------------------------------------------------------------------

* 프로그램의 기능 : 학생정보 보기, 학과별 보기, 추가, 삭제, 파일로 저장, 파일 불러오기 기능을 구현
                   (학생 추가 시, 기존 학생과 학번이 같으면 추가되지 않음)
                   
* 필요한 정보 : '학생'은 학번, 이름, 학년, 평점 정보를 가짐

----------------------------------------------------------------------------------

* 구현

 (1) 전체학생목록</br>
    => Hashtable의 모든 Objects 출력</br>
    
 (2) 학과학생목록</br>
    => Hashtable Objects들의 String Field인 '학번' 에서 subString()을 사용해 학과코드 비교 후, 일치하는 Objects을 출력</br>
    
 (3) 학생추가</br>
    => String 형식으로 학번입력 받기 (Scanner 사용)</br>
    => String 형식으로 이름입력 받기 (Scanner 사용)</br>
    => Int 형식으로 학년입력 받기 (Scanner 사용)</br>
    => double 형식으로 평점입력 받기 (Scanner 사용)</br>
    => 입력받은 데이터를 매개변수로 하는 Student 객체를 생성하여 Hashtable에 추가하기</br>
    </br>
 (4) 학생삭제</br>
    => String 형식으로 학번입력 받기 (Scanner 사용)</br>
    => Hashtable Objects들의 String Field인 '학번'을 비교 후, 일치하는 Objects을 삭제하기</br>
       
 (5) 저장</br>
    => String 형식으로 저장할 파일명입력 받기 (Scanner 사용)</br>
    => ObjectInputStream 을 사용해 File의 내용을 Hashtable에 저장</br>
 
 (6) 불러오기</br>
    => String 형식으로 불러올 파일명입력 받기 (Scanner 사용)</br>
    => ObjectOutputStream 을 사용해 Hashtable의 내용을 file로 저장</br>
 
 (7) 끝내기</br>
    => 프로그램 종료</br>
 
----------------------------------------------------------------------------------

* 사용한 주요 API
    - 학생목록 담기 : Hashtable</br>
    - 학생목록 파일 불러오기 : ObjectInputStream</br>
    - 학생목록 파일 저장하기 : ObjectOutputStream</br>

* 필요한 클래스
    - Class Main { }

    - Class Student {</br>
        <Field></br>
            String 학번;</br>
            String 이름;</br>
            int 학년;</br>
            double 평점;</br>
        
        <Method></br>
            equals();</br>
            hashCode();</br>
    }
    
    - Class StudentManager {</br>
        <Field></br>
            StudentHashtable;</br>
    
        <Method></br>
            run();</br>
    }
     
    - Class StudentHashtable {</br>
        <Field></br>
        
        <Method></br>
            showStudent();</br>
            AllStudent();</br>
            MajorStudent();</br>
            addStudent();</br>
    }
 
 
    - Class StudentFileIO {</br>
        <Field></br>
        
        <Method></br>
    }

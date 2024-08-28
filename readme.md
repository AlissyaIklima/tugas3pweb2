# MODUL 5 6

Didalam modul kali ini kita lebih dalam memahami tentang konsep Inheritance. Dan menerapkan Polymorphidm supaya mencapai fleksibilitas. Mempelajari lebih lanjut menerapkan Encapsulation agar melindungu data yang berada didalam objek. Dan mengimplementasikan bertujuan agar kode lebih sederhana dan mudah dipahami.
## Jobsheet 3: Mampu Menerapkan Konsep Inheritance, Polymorphism, Encapsulation, dan Abstraction dalam PHP
## job Tugas Studikasus Dosen

```php
<?php
// class
// class termasuk template untuk objek yang mempiliki poperti
class Person {
    protected $name;

    public function __construct($name) {
        $this->name = $name;
    }

    public function getName() {
        return $this->name;
    }
}

// Kelas Student yang mewarisi dari Person
class Student extends Person {
    public $studentID;

    public function __construct($name, $studentID) {
        parent::__construct($name);
        $this->studentID = $studentID;
    }

    // Override metode getName untuk memberikan format khusus pada Student
    public function getName() {
        return "Student: " . $this->name;
    }

    public function getStudentID() {
        return $this->studentID;
    }
}

// Kelas Teacher yang juga mewarisi dari Person
class Teacher extends Person {
    public $teacherID;

    public function __construct($name, $teacherID) {
        parent::__construct($name);
        $this->teacherID = $teacherID;
    }

    // Override metode getName untuk memberikan format khusus pada Teacher
    public function getName() {
        return "Teacher: " . $this->name;
    }

    public function getTeacherID() {
        return $this->teacherID;
    }
}

// Contoh penggunaan
$student = new Student("Alissya Iklima Nur Ramadani", "101005");
$teacher = new Teacher("Muhammad Arya Candra Pratama", "170104");

echo $student->getName() . "<br>";
echo $teacher->getName() . "<br>"; 
?>

```
## OUTPUT
```bash
Student: Alissya Iklima Nur Ramadani
Teacher: Muhammad Arya Candra Pratama
```
## Keterangan Output
class student akan diwariskan dengan class person yang dimana nanti akan dipanggil oleh objek baru dan objek baru tersebut akan menampilkan hasil implementasi student dengan getNama(), lalu metode construct() akan memunculkan apa yang ada di metode getNama() yang dipanggil kembali, begitu juga dengan teacher.
## Referensi Kode

[COM](https://www.warungbelajar.com/)
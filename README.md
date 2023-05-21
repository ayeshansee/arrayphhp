<?php

$numberOfStudents = 15;

$marks = array(
    array('English' => 40, 'Science' => 70, 'Maths' => 40, 'urdu' => 100),
    array('English' => 70, 'Science' => 30, 'Maths' => 50, 'urdu' => 200),
      array('English' => 20, 'Science' => 70, 'Maths' => 60, 'urdu' => 80),
        array('English' => 40, 'Science' => 60, 'Maths' => 50, 'urdu' => 50),
          array('English' => 35, 'Science' => 35, 'Maths' => 80, 'urdu' => 100),
            array('English' => 90, 'Science' => 80, 'Maths' => 180, 'urdu' => 100), 
              array('English' => 90, 'Science' => 80, 'Maths' => 180, 'urdu' => 100),
                array('English' => 90, 'Science' => 80, 'Maths' => 180, 'urdu' => 100),
                  array('English' => 90, 'Science' => 80, 'Maths' => 180, 'urdu' => 100),
                   array('English' => 90, 'Science' => 80, 'Maths' => 180, 'urdu' => 100),
                    array('English' => 90, 'Science' => 80, 'Maths' => 150, 'urdu' => 100),
                     array('English' => 90, 'Science' => 80, 'Maths' => 150, 'urdu' => 100),
                      array('English' => 90, 'Science' => 80, 'Maths' => 150, 'urdu' => 100),
                       array('English' => 90, 'Science' => 80, 'Maths' => 150, 'urdu' => 100),
                        array('English' => 90, 'Science' => 80, 'Maths' => 150, 'urdu' => 100),
    
);

               // Calculate and display the marks for each student

for ($i = 0; $i < $numberOfStudents; $i++) {$studentMarks = $marks[$i];

    $totalMarks = array_sum($studentMarks);

    echo "Total Marks for student " . ($i + 1) . " are: " . $totalMarks . "<br>";

}


                // Calculate and display the average English marks for the whole class

$totalEnglishMarks = 0;
foreach ($marks as $studentMarks) {
    $totalEnglishMarks += $studentMarks['English'];
}
$averageEnglishMarks = $totalEnglishMarks / $numberOfStudents;
echo "Average English marks for the whole class: " . $averageEnglishMarks . "<br>";

               // Calculate and display the average Science marks for the whole class

$totalScienceMarks = 0;
foreach ($marks as $studentMarks) {
    $totalScienceMarks += $studentMarks['Science'];
}
$averageScienceMarks = $totalScienceMarks / $numberOfStudents;
echo "Average science marks for the whole class: " . $averageScienceMarks . "<br>";
                
                 // Calculate and display the average Math marks for the whole class

$totalMathsMarks = 0;
foreach ($marks as $studentMarks) {
    $totalMathsMarks += $studentMarks['Maths'];
}
$averageMathsMarks = $totalMathsMarks / $numberOfStudents;
echo "Average science marks for the whole class: " . $averageScienceMarks . "<br>";


// Calculate and display the result for specific subjects 
//(e.g., English and Maths science )
$subject1 = 'English';
$subject2 = 'Maths';
$subject3 = 'Science';
for ($i = 0; $i < $numberOfStudents; $i++) {
    $studentMarks = $marks[$i];
    $subject1Marks = $studentMarks[$subject1];
    $subject2Marks = $studentMarks[$subject2];
    $subject3Marks = $studentMarks[$subject3];
    $result = $subject1Marks+$subject2Marks+$subject3Marks;
    echo "Result for student " . ($i + 1) . " in $subject1 and $subject2 and $subject3 $result "."<br>";
}


?>

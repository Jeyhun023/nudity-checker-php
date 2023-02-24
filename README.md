# PHP nudity and porn image detector

PHP code by Jeyhun Rashidov from Azerbaijan:

### Sample database design for Users.

### Usage

**checkimage.php**
```php
<?php
    //---Image Filter Code
    require_once('class.ImageFilter.php');
    $filter = new ImageFilter();
    $score = $filter->GetScore($_FILES['photoimg']['tmp_name']);
    if($score >= 60) // Score value If more than 60%, it consider as adult image. 
    {
        echo "Image scored ".$score."%, It seems that you have uploaded a nude picture :-(";
    } else {
        echo "Image don't contain nudity";
    }
?>
```

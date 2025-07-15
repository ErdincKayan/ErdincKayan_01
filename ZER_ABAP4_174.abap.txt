REPORT zer_abap4_174.

*Class;Kullanıcıdan currcode(scarr) isteyin, gelen currcoda göre scarr tablosundan bilgi çekin, daha sonra sbook tablosundan carrid, bookid, customid verilerini scarrdan
*çektiğiniz tablodaki carrid verilerine göre For all entries ile çekin ve gösterim sağlayın.

PARAMETERS p_crcode TYPE s_currcode.

DATA: go_class TYPE REF TO zer_cl_05.

START-OF-SELECTION.

  CREATE OBJECT go_class.

  go_class->sbook( iv_currcode = p_crcode ).
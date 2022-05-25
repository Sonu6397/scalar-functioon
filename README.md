# scalar-functioon


==============================function without parameter===========================scalar function==========================
create function number()
returns varchar(100)
as
begin
return 'welcome to function'
end
select dbo.number()
==============================function of single parameter=========================
create function showmesaage(@num as int)
returns int
as
begin
return (@num * @num)
end
select dbo. showmesaage(4)
=============================function of multpiple parameter===========================
create function cheknumer(@age1 as int, @age2 as int )
returns money
as
begin
return (@age1 * @age2)
end
select dbo. cheknumer(4,7)
==============================condition=================================================
create function sonu(@age as int)
returns varchar(100)
as
begin
       declare @str varchar(100)
	   if @age >= 18
	   begin
	       set @str='you are eligible to for vote'
		   end
		   else
		   begin 
		   set @str ='you aree not eligible top for vote'
		   end
		   return @str
		   
end
select dbo.sonu(12)
select dbo.sonu(19)



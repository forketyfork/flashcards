START
Basic
Front: How does Django's `bulk_create` help with insert conflicts?
Back: By using `bulk_create` with `ignore_conflicts=True`, Django generates `INSERT ... ON CONFLICT DO NOTHING` statements, reducing overhead from exceptions and rollbacks.
<!--ID: 1751110154910-->
END

START
Basic
Front: Why might raw SQL be preferred over Django ORM for handling insert conflicts?
Back: Raw SQL allows direct use of `ON CONFLICT DO NOTHING` without ORM overhead, providing better performance and more control over conflict handling.
<!--ID: 1751110154912-->
END

START
Basic
Front: How can raw SQL be used in Django to handle insert conflicts?
Back: By executing an `INSERT INTO ... ON CONFLICT DO NOTHING` statement using Django's database cursor for better performance and control.
<!--ID: 1751110154913-->
END 
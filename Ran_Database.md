provider "aws" {
  region = "us-west-2"
}

resource "aws_db_instance" "example" {
  allocated_storage    = 20
  engine               = "mysql"
  engine_version       = "8.0"
  instance_class       = "db.t2.micro"
  name                 = "exampledb"
  username             = "RanShell"
  password             = "Text@123321"
  parameter_group_name = "default.mysql8.0"
  skip_final_snapshot  = true
}

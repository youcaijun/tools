# tools

--------------------------
处理字符串

形如"2019-1-1-汉字.xlsx" 
输出结果为 2019-01-01

public static void main(String[] args) {
		String filename ="2019-1-1-汉字.xlsx";
		int xx = filename.lastIndexOf("-");
		filename = filename.substring(0,xx);
		String[] datestr =filename.split("-");
		if(datestr[1].length()<2) {
			datestr[1] = "0"+datestr[1];
		}
		if(datestr[2].length()<2) {
			datestr[2] = "0"+datestr[2];
		}
		String date = datestr[0]+"-"+datestr[1]+"-"+datestr[2];
		System.out.println(date);
	}

------------------------
读取文件夹下所有文件
# fast_xlsx
A fast xlsx reader for pandas

Reads an .xlsx or .xlsm file and returns a Pandas DataFrame. Is much faster than pandas.read_excel().

  Parameters
  ----------
  path : str
      The path to the .xlsx or .xlsm file.
      
  sheet_name : str, optional
      Name of the sheet to read. If none, the first (not the active!) sheet is read. The default is None.
      
  header : bool, optional
      Whether to use the first line as column headers. The default is True.
      
  index_col : bool, optional
      Whether to use the first column as index. The default is False.
      
  skiprows : list of int, optional.
      The row numbers to skip ([0, 1] skips the first two rows). The default is [].
      
  skipcolumns : list of int, optional.
      The column numbers to skip ([0, 1] skips the first two columns). The default is [].

  Raises
  ------
  TypeError
      If the file is no .xlsx or .xlsm file.
  FileNotFoundError
      If the sheet name is not found.

  Returns
  -------
  Pandas DataFrame
      The input file as DataFrame.

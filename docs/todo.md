# Ideas for Future Work

- Consider adding a simple Python module in a `tomes_eaxs` sub-folder so that other TOMES Python packages can import the namespace URI, namespace prefix, and XSD locations without having to hardcode them:

		#tomes_eaxs.py
		class EAXS():
		    def __init__(self, version=1, prefix="eaxs"):
		            self.version = version
		            self.prefix = prefix
		            self._url = "https://{domain}.com/StateArchivesOfNorthCarolina/tomes-eaxs"
		            self.ns = self._url.format(domain="github")
		            self.xsd = "{domain}/master/versions/{version}/eaxs_schema_v{version}.xsd".format(
		                domain=self._url.format(domain="raw.githubusercontent"), version=self.version)
		            self.json_schema = self.xsd.replace(".xsd", ".json")
		    """
		    Example:
		    >>> from tomes_eaxs import EAXS
		    >>> eaxs = EAXS()
		    >>> eaxs.version # 1
		    >>> print(eaxs.xsd) # version "1" string.
		    >>> eaxs = EAXS(version=2)
		    >>> eaxs.version # 2
		    >>> print(eaxs.xsd) # version "2" string.
		    """
    
	This module should include a `setup.py` file but the actual XSD/JSON files should be excluded from the Python package.
